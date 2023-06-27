# OOPJ-College Program-18

## Write a program that moves a circle up, down, left or right using  arrow keys. 

```JAVA
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.input.KeyCode;
import javafx.scene.layout.Pane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Circle;
import javafx.stage.Stage;

public class CircleMovement extends Application {

    private static final int CIRCLE_RADIUS = 50;
    private static final int CIRCLE_SPEED = 10;

    private Circle circle;

    @Override
    public void start(Stage primaryStage) {
        circle = createCircle();

        Pane root = new Pane(circle);
        Scene scene = new Scene(root, 400, 400);

        scene.setOnKeyPressed(e -> handleKeyPress(e.getCode()));
        scene.setOnKeyReleased(e -> handleKeyRelease(e.getCode()));

        primaryStage.setTitle("Circle Movement");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    private Circle createCircle() {
        Circle circle = new Circle(CIRCLE_RADIUS);
        circle.setFill(Color.BLUE);
        circle.setCenterX(200);
        circle.setCenterY(200);
        return circle;
    }

    private void handleKeyPress(KeyCode keyCode) {
        switch (keyCode) {
            case UP:
                circle.setCenterY(circle.getCenterY() - CIRCLE_SPEED);
                break;
            case DOWN:
                circle.setCenterY(circle.getCenterY() + CIRCLE_SPEED);
                break;
            case LEFT:
                circle.setCenterX(circle.getCenterX() - CIRCLE_SPEED);
                break;
            case RIGHT:
                circle.setCenterX(circle.getCenterX() + CIRCLE_SPEED);
                break;
            default:
                break;
        }
    }

    private void handleKeyRelease(KeyCode keyCode) {
        // Add any additional key release handling here
    }

    public static void main(String[] args) {
        launch(args);
    }
}

```

```

```
