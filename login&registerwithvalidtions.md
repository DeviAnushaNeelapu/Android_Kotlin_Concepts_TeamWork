![otpss](https://user-images.githubusercontent.com/46557268/139210988-25c89213-8731-479b-b62c-9a26ff9d68ed.JPG)
```
<?xml version="1.0" encoding="utf-8"?>
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
```
package com.example.sravs.first

import android.content.Intent
import android.support.v7.app.AppCompatActivity
import android.os.Bundle
import android.view.View
import android.widget.TextView
import android.widget.EditText

import android.widget.Button
import android.widget.Toast

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)


        //Linking of UI Component
        val loginButton : Button = findViewById(R.id.btn_login)
        val regButton : Button = findViewById(R.id.btn_register)

        var usrTXTObj : EditText = findViewById(R.id.username)
        var passTXTObj : EditText = findViewById(R.id.password)


        loginButton.setOnClickListener {

            if(usrTXTObj.text.toString().equals("admin") && passTXTObj.text.toString().equals("admin")) {
                val accountIntent = Intent(this, Account::class.java)
                startActivity(accountIntent)
            }else{

                Toast.makeText(this,"Unsuccessful",Toast.LENGTH_SHORT).show()
            }
        }
        regButton.setOnClickListener {
            val registerIntent = Intent(this,register::class.java)
            startActivity(registerIntent)
        }
    }





}

```
## account
```
<?xml version="1.0" encoding="utf-8"?>
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
## register
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
