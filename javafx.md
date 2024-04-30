---
marp: true
---

# Introducción a JavaFX

---

## ¿Qué es JavaFX?

- JavaFX es un conjunto de bibliotecas y herramientas para crear aplicaciones de escritorio y aplicaciones RIA (Rich Internet Applications) en Java.
- Proporciona una API rica y moderna para la creación de interfaces de usuario interactivas.
- Es una alternativa a la biblioteca de GUI Swing y ofrece características avanzadas como gráficos en 2D y 3D, animaciones, CSS, eventos y mucho más.

---

## Características de JavaFX

- Diseño declarativo mediante archivos FXML.
- Separación clara entre la lógica de la aplicación y la presentación.
- Soporte completo para gráficos en 2D y 3D.
- Animaciones y efectos visuales.
- Estilos y temas personalizables mediante CSS.
- Eventos y enlace de datos.
- Integración con la plataforma Java y otras tecnologías.

---

## Estructura básica de una aplicación JavaFX

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Label;
import javafx.scene.layout.StackPane;
import javafx.stage.Stage;

public class HelloWorldApp extends Application {

    public static void main(String[] args) {
        launch(args);
    }

    @Override
    public void start(Stage primaryStage) {
        Label label = new Label("¡Hola, mundo!");
        StackPane root = new StackPane(label);
        Scene scene = new Scene(root, 300, 200);
        primaryStage.setScene(scene);
        primaryStage.setTitle("Hola JavaFX");
        primaryStage.show();
    }
}

```

---

---
marp: true
---

# Botones y Reacciones en JavaFX

---

## Botones en JavaFX

- JavaFX proporciona la clase `Button` para crear botones en la interfaz de usuario.
- Los botones pueden tener texto o iconos, y se pueden personalizar mediante CSS.
- Se pueden agregar controladores de eventos a los botones para responder a las interacciones del usuario.

Ejemplo de código:

```java
Button button = new Button("Haz clic");
button.setOnAction(e -> {
    System.out.println("¡Haz hecho clic en el botón!");
});

```

---

## Reacciones a eventos
- Los botones (y otros controles) pueden tener acciones asociadas a ellos.
- Se pueden definir controladores de eventos para responder a los diferentes eventos, como clics de botón, cambios de valor, etc.
Los controladores de eventos se implementan mediante la interfaz EventHandler.

```java
Button button = new Button("Haz clic");
button.setOnAction(new EventHandler<ActionEvent>() {
    @Override
    public void handle(ActionEvent event) {
        System.out.println("¡Has hecho clic en el botón!");
    }
});

```

---

```java
import javafx.application.Application;
import javafx.event.ActionEvent;
import javafx.event.EventHandler;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.layout.StackPane;
import javafx.stage.Stage;

public class ButtonExampleApp extends Application {

    public static void main(String[] args) {
        launch(args);
    }

    @Override
    public void start(Stage primaryStage) {
        Button button = new Button("Haz clic");
        button.setOnAction(new EventHandler<ActionEvent>() {
            @Override
            public void handle(ActionEvent event) {
                System.out.println("¡Has hecho clic en el botón!");
            }
        });

        StackPane root = new StackPane(button);
        Scene scene = new Scene(root, 300, 200);

        primaryStage.setScene(scene);
        primaryStage.setTitle("Ejemplo de Botón en JavaFX");
        primaryStage.show();
    }
}
```