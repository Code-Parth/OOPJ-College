# OOPJ-College Program-17

## Write a program that displays a tic-tac-toe board. A cell may be X,  O, or empty. What to display at each cell is randomly decided. The  X and O are images in the files X.gif and O.gif.

```JAVA
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.image.Image;
import javafx.scene.image.ImageView;
import javafx.scene.layout.GridPane;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;
import java.io.FileInputStream;
import java.io.FileNotFoundException;

public class TicTacToeBoard extends Application {
    public void start(Stage primaryStage) throws Exception {
        primaryStage.setTitle("Tic-Tac-Toe");
        GridPane gridPane = new GridPane();
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                int n = (int) (Math.random() * 3);
                if (n == 0)
                    gridPane.add(createX(), i, j);
                else if (n == 1)
                    gridPane.add(createO(), i, j);
                else
                    continue;
            }
        }
        Scene primaryScene = new Scene(gridPane, 300, 300);
        primaryStage.setScene(primaryScene);
        primaryStage.show();
    }

    public VBox createX() throws FileNotFoundException {
        // put the address of cross gif.
        Image imageX = new Image(new FileInputStream("D:\\Sem 4\\java programs\\JAVAFX\\cross.gif"));
        ImageView imageViewX = new ImageView(imageX);
        VBox xBox = setProp(imageViewX);
        return xBox;
    }

    public VBox createO() throws FileNotFoundException {
        // put the address of circle gif.
        Image imageO = new Image(new FileInputStream("D:\\Sem 4\\java programs\\JAVAFX\\circle.gif"));
        ImageView imageViewO = new ImageView(imageO);
        VBox oBox = setProp(imageViewO);
        return oBox;
    }

    public VBox setProp(ImageView iv) {
        iv.setFitHeight(50);
        iv.setFitWidth(50);
        iv.setPreserveRatio(true);
        VBox vBox = new VBox();
        vBox.getChildren().add(iv);
        vBox.setStyle("-fx-border-color: orange");
        return vBox;
    }

    public static void main(String[] args) {
        Application.launch(args);
    }
}

```

![image](https://github.com/Code-Parth/OOPJ-College/assets/84669955/26ef155f-a6b1-4c8d-bab4-4158d31444c2)

