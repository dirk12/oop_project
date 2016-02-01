package application;
import javafx.application.Application;
import javafx.event.ActionEvent;
import javafx.event.EventHandler;
import javafx.geometry.Insets;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.control.Label;
import javafx.scene.control.TextArea;
import javafx.scene.control.TextField;
import javafx.scene.layout.GridPane;
import javafx.scene.paint.Color;
import javafx.stage.Modality;
import javafx.stage.Stage;

public class Main extends Application {
    
    Stage window, window2, windowLogin;
    Scene scene, scene2, scene3;
    TextField wordInput;
    TextArea textA;
    GridPane grid2, grid3;
    
    @Override
	    public void start(Stage primaryStage) throws Exception {
	    	window = primaryStage;
	    	window.setTitle("Translator");
	    	window.setResizable(false);
	    	
		    Stage secondaryStage = new Stage();
		    window2 = secondaryStage;
		    window2.setTitle("Translator");
		    window2.setResizable(false);
		    
		    Stage tertiaryStage = new Stage();
		    windowLogin = tertiaryStage;
		    windowLogin.setTitle("Login");
		    windowLogin.setResizable(false);
		    //windowLogin.initModality(Modality.WINDOW_MODAL);
	    
		    //GridPane
		    GridPane grid = new GridPane();
		    grid.setPadding(new Insets(10, 10, 10, 10));
		    grid.setVgap(8);//vertical spacing 8 pixels
		    grid.setHgap(10);//horizontal spacing 10 pixels
	
		    //GridPane2
		    grid2 = new GridPane();
		    grid2.setPadding(new Insets(10, 10, 10, 10));
		    grid2.setVgap(8);//vertical spacing 8 pixels
		    grid2.setHgap(10);//horizontal spacing 10 pixels
		    scene2 = new Scene(grid2, 550, 250);
		    scene2.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
		    
		    //GridPane3 (Login)
		    grid3 = new GridPane();
		    grid3.setPadding(new Insets(10, 10, 10, 10));
		    grid3.setVgap(8);//vertical spacing 8 pixels
		    grid3.setHgap(10);//horizontal spacing 10 pixels
		    scene3 = new Scene(grid3, 340, 150);
		    scene3.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
		    
		    //Name Label - constrains use (child, column, row)
		    Label welcomeLabel = new Label("");
		    welcomeLabel.setTextFill(Color.web("#FFFFFF")); //Change Color of this Label
		    GridPane.setConstraints(welcomeLabel, 1, 0);
		    
		    //Word Input
		    wordInput = new TextField("");
		    GridPane.setConstraints(wordInput, 1, 0);
		    
		    //Translate Button
		    Button translateButton1 = new Button("Translate");
		    translateButton1.setTextFill(Color.web("#000000"));
		    translateButton1.setOnAction(null);
		    GridPane.setConstraints(translateButton1, 1, 2);
		    translateButton1.setOnAction(new EventHandler<ActionEvent>() {
		
		        @Override
		        public void handle(ActionEvent t) {
		            startTranslation();
		        }
			    });
		    
		    //Clear Button
		    Button clearButton = new Button("Clear");
		    GridPane.setConstraints(clearButton, 1, 3);
		    clearButton.setOnAction(new EventHandler<ActionEvent>() {
		
		        @Override
		        public void handle(ActionEvent t) {
		            wordInput.setText("");
		        }
		    });
	
		    //Exit Button
		    Button exitButton = new Button("Exit");
		    exitButton.setText("Exit");
		    exitButton.setTextFill(Color.web("#000000"));
		    GridPane.setConstraints(exitButton, 2, 4);
		    exitButton.setOnAction(new EventHandler<ActionEvent>() {
		
		        @Override
		        public void handle(ActionEvent t) {
		            System.exit(0);
		        }
		    });
		   // exitButton.setOnAction(e -> System.exit(0));
		    
		    scene = new Scene(grid, 260, 150);//Placed it here so I can use it in Grid2
		    scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
		    window.setScene(scene);
		    window.show();
		    
		    //Back Button
		    Button backButton = new Button("Back");
		    GridPane.setConstraints(backButton, 1, 3);
		    backButton.setOnAction(new EventHandler<ActionEvent>() {
		
		    @Override
	        public void handle(ActionEvent t) {
	            textA.clear();
	            window2.close();
		        }
		    });
	    
		    //Name Label - constrains use (child, column, row)
		    Label sucLabel = new Label("Here is the translation!");
		    GridPane.setConstraints(sucLabel, 1, 0);
		    
		    //----------------------------------------------------------------------------------------
		    
		    //User Name Label
		    Label username = new Label("Username:");
		    GridPane.setConstraints(username, 0, 0);
		    
		    //User Name Text Field
		    TextField usernameInput = new TextField("");
		    //usernameInput.setPromptText("username");
		    GridPane.setConstraints(usernameInput, 1, 0);
		    
		    //Password Label
		    Label password = new Label("Password:");
		    GridPane.setConstraints(password, 0, 1);
		    
		    //User Name Text Field
		    TextField passwordInput = new TextField("");
		    //passwordInput.setPromptText("password");
		    GridPane.setConstraints(passwordInput, 1, 1);
		    
		    //Login Button
		    Button loginButton = new Button("Log In");
		    GridPane.setConstraints(loginButton, 1, 2);
		    //loginButton.setOnAction(new EventHandler<ActionEvent>() {};
		    
		    //Exit Button (Login Scene)
		    Button exitButtonLoginScene = new Button("Exit");
		    exitButtonLoginScene.setText("Exit");
		    exitButtonLoginScene.setTextFill(Color.web("#000000"));
		    GridPane.setConstraints(exitButtonLoginScene, 2, 4);
		    exitButtonLoginScene.setOnAction(new EventHandler<ActionEvent>() {
		
		        @Override
		        public void handle(ActionEvent t) {
		            System.exit(0);
		        }
		    });

		    //Add everything to search window (grid)
		    grid.getChildren().addAll(welcomeLabel, wordInput, translateButton1, clearButton, exitButton);
		    
		    //Add everything to the output window (grid2)
		    grid2.getChildren().add(backButton);
		    grid2.getChildren().add(sucLabel);
		    
		    
		    //Add everything to the login window (grid3)
		    grid3.getChildren().add(username);
		    grid3.getChildren().add(usernameInput);
		    grid3.getChildren().add(password);
		    grid3.getChildren().add(passwordInput);
		    grid3.getChildren().add(loginButton);
		    grid3.getChildren().add(exitButtonLoginScene);
		    
		    windowLogin.setScene(scene3);
		    windowLogin.show();
	 	}

		    public void startTranslation(){
		       	String string1, string2;
		        string1 = wordInput.getText(); 
		        if (string1.equals("Affe")){
		        	string2 = "Monkey"; 
		        }else{
		            if (string1.equals("Wasser")){
		            	string2 = "Water"; 
		        }else{
		                string2 = "Word is not in dictionary!";
		            }
		        }
		        //string2 = translate.execute(string1, Language.ENGLISH, Language.GERMAN);
		        textA = new TextArea(string2);
		        GridPane.setConstraints(textA, 1, 1);
		        window2.setScene(scene2);
		        grid2.getChildren().add(textA);//
		        window2.show();
		   }
		
		    
	       public static void main(String[] args) {
	    	   launch(args);
	       }
}
