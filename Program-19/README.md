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

```

```
