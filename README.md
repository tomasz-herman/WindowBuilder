# WindowBuilder

Window Builder for Java Swing.  
Simplifies creating JFrames and JDialogs. 
Provides useful defaults and simplifies setting more complicated options like opacity or fullscreen mode.

# Examples

### Creating JFrame

```java
JFrame window = new WindowBuilder()
        .setContentPane(mainLayout.getMainPane())
        .setPreferredSize(1280, 720)
        .setMinimumSize(320, 240)
        .setMenuBar(mainLayout.getMenuBar())
        .setTitle("Project")
        .setImageIcon(ICON.getImage())
        .setMaximized(true)
        .setNothingOnClose()
        .buildFrame();
```

### Creating JDialog

```java
JDialog dialog = new WindowBuilder()
        .setContentPane(new TextLayout(text).getMainPanel())
        .setTitle(title)
        .setResizable(false)
        .setDocumentModal()
        .setOwner((JFrame) SwingUtilities.getWindowAncestor(mainPane))
        .buildDialog();
```

# Using in your own project

### Gradle

Add the repository to your repositories section:
```groovy
repositories {
    maven {
        url = uri('https://maven.pkg.github.com/tomasz-herman/WindowBuilder')
        credentials {
            username = "token"
            password = "\u0033\u0038\u0038\u0063\u0034\u0034\u0062\u0039\u0037\u0034\u0032\u0035\u0065\u0061\u0036\u0065\u0064\u0066\u0031\u0065\u0030\u0033\u0039\u0032\u0066\u0063\u0064\u0031\u0064\u0065\u0031\u0039\u0036\u0039\u0038\u0064\u0064\u0039\u0039\u0061"
        }
    }
}
```
Then add the dependency:
```groovy
dependencies {
    implementation 'com.hermant:windowbuilder:1.0.2'
}
```
