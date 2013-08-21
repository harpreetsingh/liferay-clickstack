First cut of Liferay ClickStack. 

1. Expects a Liferay zip in a directory called /Users/harpreet/liferay/liferay*.zip

```cd liferay_plugin
   make compile```
   
   This creates a zip called cb_liferay.zip, copy to liferay_plugin directory
  
2. Run genapp
    ```genapp:deploy("PATH_TO_test_app/").

3. cd $APP_ID/control/start
