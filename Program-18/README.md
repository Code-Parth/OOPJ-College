# OOPJ-College Program-18

## Write a program that moves a circle up, down, left or right using  arrow keys. 

```JAVA
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.shape.Circle;
import javafx.scene.layout.Pane;
import javafx.geometry.Insets;
import javafx.stage.Stage;

public class CircleMovement extends Application {
    public void start(Stage primaryStage) {
        Pane pane = new Pane();
        pane.setPadding(new Insets(30, 30, 30, 30));
        Circle circle = new Circle(30, 30, 30);
        pane.getChildren().add(circle);
        pane.setOnKeyPressed(e -> {

            switch (e.getCode()) {
                case UP:
                    circle.setCenterY(
                            circle.getCenterY() > circle.getRadius() ? circle.getCenterY() - 15 : circle.getCenterY());
                    break;
                case DOWN:
                    circle.setCenterY(
                            circle.getCenterY() < pane.getHeight() - circle.getRadius() ? circle.getCenterY() + 15
                                    : circle.getCenterY());
                    break;
                case LEFT:
                    circle.setCenterX(
                            circle.getCenterX() > circle.getRadius() ? circle.getCenterX() - 15 : circle.getCenterX());
                    break;
                case RIGHT:
                    circle.setCenterX(
                            circle.getCenterX() < pane.getWidth() - circle.getRadius() ? circle.getCenterX() + 15
                                    : circle.getCenterX());
            }
        });
        Scene scene = new Scene(pane, 200, 200);
        primaryStage.setTitle("p52");
        primaryStage.setScene(scene);
        primaryStage.show();
        pane.requestFocus();
    }
}

```

|||
|--------|-------|
| Actual | Right Arrow |
| ![image](https://github.com/Code-Parth/OOPJ-College/assets/84669955/4a07c162-eada-4c6c-b85b-2b9196761281) | ![image](https://github.com/Code-Parth/OOPJ-College/assets/84669955/91dd7207-b3d6-452c-ab13-aeaeaa765458) |
| Down Arrow | Left Arrow |
| ![image](https://github.com/Code-Parth/OOPJ-College/assets/84669955/3e1cceac-ea2c-43d2-bf6b-140c808c7afa) | ![image](https://github.com/Code-Parth/OOPJ-College/assets/84669955/f77a4b0b-bddd-4f23-9be9-35b2a5359a9a) |
