# OOPJ-College Program-17

## Write a program that displays a tic-tac-toe board. A cell may be X,  O, or empty. What to display at each cell is randomly decided. The  X and O are images in the files X.gif and O.gif.

```JAVA
import javafx.application.Application;
import javafx.geometry.Pos;
import javafx.scene.Scene;
import javafx.scene.image.Image;
import javafx.scene.image.ImageView;
import javafx.scene.layout.GridPane;
import javafx.stage.Stage;

import java.util.Random;

public class TicTacToeBoard extends Application {
    private static final int BOARD_SIZE = 3;
    private static final String[] CELL_VALUES = {"X", "O", ""};

    @Override
    public void start(Stage primaryStage) {
        primaryStage.setTitle("Tic-Tac-Toe Board");

        // Create a random generator
        Random random = new Random();

        // Create a grid pane to hold the cells
        GridPane gridPane = new GridPane();
        gridPane.setAlignment(Pos.CENTER);
        gridPane.setHgap(10);
        gridPane.setVgap(10);

        // Populate the cells with random values
        for (int row = 0; row < BOARD_SIZE; row++) {
            for (int col = 0; col < BOARD_SIZE; col++) {
                // Get a random cell value
                String cellValue = CELL_VALUES[random.nextInt(CELL_VALUES.length)];

                // Create an ImageView with the appropriate image
                ImageView imageView = new ImageView();
                if (cellValue.equals("X")) {
                    imageView.setImage(new Image("X.gif"));
                } else if (cellValue.equals("O")) {
                    imageView.setImage(new Image("O.gif"));
                }

                // Add the ImageView to the grid pane
                gridPane.add(imageView, col, row);
            }
        }

        // Create a scene with the grid pane
        Scene scene = new Scene(gridPane, 300, 300);

        // Set the scene on the primary stage and show it
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}

```

```

```
