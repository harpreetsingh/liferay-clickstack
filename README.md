First cut of Liferay ClickStack. 

Expects a Liferay zip in a directory called /Users/harpreet/liferay/liferay*.zip

    cd liferay_plugin
    make compile'
   
This creates a zip called cb_liferay.zip, copy to liferay_plugin directory
  
Run genapp

    genapp:deploy("PATH_TO_test_app/").
    cd $APP_ID/control/start'
