# ElementFX

ElementUi in javafx,that you can get a beautiful applications with only one line code.

JavaFX版本的ElementUi，您可以仅需一行代码而轻松美化您的JavaFX应用

Using:

For Java:
```
        Scene scene = new Scene(root);
        scene.getStylesheets().add(CssResources.globalCssFile);
        /*
        or：
        CssResourcesKt.themes(scene, (strings, cssResources) -> {
            strings.add(CssResources.globalCssFile);
            strings.add(CssResources.buttonCssFile);//可选，用于每个组件可单独调整主题
            return null;
        });
        */
        primaryStage.setScene(scene);
        primaryStage.setTitle("ElementForJavaFX");
        primaryStage.show();
```


For Kotlin:

```
    primaryStage.run {
        scene = Scene(root,400.0,400.0).apply {
            themes {
                this += it.globalCssFile
                this += it.buttonCssFile//可选，用于每个组件可单独调整主题
            }
        }
        title = "ElementForJavaFX"
        show()
    }
```

todo:
为每个组件单独调整主题:
例如：
```
        val regButton = Button("Register").apply {
            theme(ElementButton.orangeButton)
        }
```

<font color="red" size="5px">当前仅支持TextField和Button</font>

当前支持的组件:

Supported nodes:
> + Button
> + TextField
> + ListView
> + TextArea
> + Label
> + ComboBox
> + CheckBox
> + ScrollPane
> + ScrollBar
> + DatePicker
> + TableView
> + Spinner
> + TabPane
> + Pagination
> + ContextMenu
> + Slider
> + ProgressBar
> + TreeView


#### 示例效果：
Demo path is : src/test/kotlin/testapp/Demo.kt

![Screen](screenshot/screen_1.0.png)
