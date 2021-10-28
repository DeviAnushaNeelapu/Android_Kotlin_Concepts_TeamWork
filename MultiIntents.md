![otp](https://user-images.githubusercontent.com/46557268/139208456-733fd174-491b-497f-9b00-d246f8d16859.JPG)
### Login Page when you click on login it will navigate to loginpage ,when you click on register it will navigate to registerpage.
## activity_main.xml
```<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:orientation="vertical"
    android:layout_gravity="center_vertical"
    tools:context=".MainActivity">

    <TextView
        android:layout_gravity="center"
        android:textSize="50sp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Login Panel"
        />
    <EditText
        android:hint="Enter username"
        android:id="@+id/username"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />
    <EditText
        android:hint="Enter password"
        android:id="@+id/password"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />
    <LinearLayout
        android:orientation="horizontal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">
    <Button
        android:id="@+id/btn_login"
        android:layout_weight="0.5"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="login"/>
    <Button
        android:id="@+id/btn_register"
        android:layout_weight="0.5"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="register"/>
</LinearLayout>
</LinearLayout>
```
## mainactivity
```package com.example.sravs.first

import android.content.Intent
import android.support.v7.app.AppCompatActivity
import android.os.Bundle
import android.view.View
import android.widget.TextView
import android.widget.Button

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        //Linking of UI Component
        val loginButton : Button = findViewById(R.id.btn_login)
        val regButton : Button = findViewById(R.id.btn_register)


        loginButton.setOnClickListener {

            val accountIntent = Intent(this,Account::class.java)
            startActivity(accountIntent)
        }
        regButton.setOnClickListener {
            val registerIntent = Intent(this,register::class.java)
            startActivity(registerIntent)
        }
    }



}
```
## loginactivity
```<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    android:orientation="vertical"
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    tools:context=".Account">
<TextView
    android:textSize="60sp"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:text="welcome login"/>
</LinearLayout>
```
## registeractivity
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    android:orientation="vertical"
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    tools:context=".register">
    <TextView
        android:textSize="60sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="welcome register"/>
</LinearLayout>
```
