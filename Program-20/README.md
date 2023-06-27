# OOPJ-College Program-20

## Write a GUI program that use button to move the message to the  left and right and use the radio button to change the color for the  message displayed. 

```JAVA
import javafx.application.Application;
import javafx.geometry.Insets;
import javafx.geometry.Pos;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.control.RadioButton;
import javafx.scene.control.ToggleGroup;
import javafx.scene.layout.HBox;
import javafx.scene.layout.VBox;
import javafx.scene.paint.Color;
import javafx.scene.text.Font;
import javafx.scene.text.Text;
import javafx.stage.Stage;

public class MessageApp extends Application {

    private static final int WINDOW_WIDTH = 400;
    private static final int WINDOW_HEIGHT = 200;

    private Text messageText;
    private String currentColor;

    public static void main(String[] args) {
        launch(args);
    }

    @Override
    public void start(Stage primaryStage) {
        messageText = new Text("Hello, JavaFX!");
        messageText.setFont(Font.font(20));

        Button leftButton = new Button("Move Left");
        leftButton.setOnAction(event -> moveMessageLeft());

        Button rightButton = new Button("Move Right");
        rightButton.setOnAction(event -> moveMessageRight());

        ToggleGroup colorGroup = new ToggleGroup();
        RadioButton redRadio = createColorRadioButton("Red", "red", colorGroup);
        RadioButton greenRadio = createColorRadioButton("Green", "green", colorGroup);
        RadioButton blueRadio = createColorRadioButton("Blue", "blue", colorGroup);

        HBox buttonBox = new HBox(10, leftButton, rightButton);
        buttonBox.setAlignment(Pos.CENTER);

        VBox root = new VBox(20, messageText, buttonBox, redRadio, greenRadio, blueRadio);
        root.setPadding(new Insets(20));
        root.setAlignment(Pos.CENTER);

        Scene scene = new Scene(root, WINDOW_WIDTH, WINDOW_HEIGHT);

        primaryStage.setTitle("Message App");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    private RadioButton createColorRadioButton(String text, String color, ToggleGroup toggleGroup) {
        RadioButton radioButton = new RadioButton(text);
        radioButton.setToggleGroup(toggleGroup);
        radioButton.setOnAction(event -> changeMessageColor(color));
        return radioButton;
    }

    private void moveMessageLeft() {
        messageText.setTranslateX(messageText.getTranslateX() - 10);
    }

    private void moveMessageRight() {
        messageText.setTranslateX(messageText.getTranslateX() + 10);
    }

    private void changeMessageColor(String color) {
        Color newColor = Color.web(color);
        messageText.setFill(newColor);
        currentColor = color;
    }
}

```

```

```
