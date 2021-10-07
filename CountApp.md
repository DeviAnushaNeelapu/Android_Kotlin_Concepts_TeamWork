 #  Count App

activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:weightSum="10"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <Button
        android:id="@+id/increment"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="1"
        android:text="Increment" />

    <TextView
        android:id="@+id/tv"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="8"
        android:textSize="150sp"
        android:gravity="center"
        android:text="0" />

    <Button
        android:id="@+id/decrement"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="1"
        android:text="Decrement" />

</LinearLayout>


package com.example.countapp

import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.widget.Button
import android.widget.TextView

class MainActivity : AppCompatActivity() {
    var counter = 0;
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        //1: Linking UI components
        var resultTVObject: TextView = findViewById(R.id.tv)
        val btnIncObject: Button = findViewById(R.id.increment)
        val btnDecObject: Button = findViewById(R.id.decrement)


        //3: Attach Listener to button object
        btnIncObject.setOnClickListener {
            counter++

            //3.1: Update the value with text view object
            resultTVObject.text = "$counter"
        }
        //4.
        btnDecObject.setOnClickListener {
            counter--

            //4.1: Update the value with text view object
            resultTVObject.text = "$counter"
        }

    }
}

