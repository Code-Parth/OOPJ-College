# OOPJ-College Program-19

## Write a program that displays the color of a circle as red when the  mouse button is pressed and as blue when the mouse button is  released.

```JAVA
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.input.MouseEvent;
import javafx.scene.layout.Pane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Circle;
import javafx.stage.Stage;

public class CircleColorChange extends Application {
    private Circle circle;

    public static void main(String[] args) {
        launch(args);
    }

    @Override
    public void start(Stage primaryStage) {
        circle = new Circle(100, Color.BLUE);
        circle.setCenterX(200);
        circle.setCenterY(200);

        Pane root = new Pane(circle);
        Scene scene = new Scene(root, 400, 400);

        scene.setOnMousePressed(this::handleMousePressed);
        scene.setOnMouseReleased(this::handleMouseReleased);

        primaryStage.setTitle("Circle Color Change");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    private void handleMousePressed(MouseEvent event) {
        circle.setFill(Color.RED);
    }

    private void handleMouseReleased(MouseEvent event) {
        circle.setFill(Color.BLUE);
    }
}

```

| Actual | OnPress(red) | OnRelease(Blue) |
|----|----|----|
| ![image](https://github.com/Code-Parth/OOPJ-College/assets/84669955/e903e680-eb95-4209-84ab-b6452a30fca9) | ![image](https://github.com/Code-Parth/OOPJ-College/assets/84669955/9eaab8e7-233f-4e24-a851-08374a099ea8) | ![image](https://github.com/Code-Parth/OOPJ-College/assets/84669955/3762f766-63bf-402b-aac3-0edd430e3961) |
