# Ex.No: 8
# Build a program to show five checkboxes and toast selected checkboxes.

## AIM:

To create a list using checkbox to display selected checkbox item using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min.required Arctic Fox)

## ALGORITHM:

Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as "check" and click Next. 

Step 3: Then select the Empty Activity and click Next. Finally click Finish.

Step 4: Design layout using UI components in activity_main.xml.

Step 5: Display the list using checkbox in MainActivity file.

Step 6: Launch an emulator and run the application.

## PROGRAM:
```
/*
Program to display "check list item”.
Developed by        : J . RITHANIEPRIYANKA
Registration Number : 212220230039
*/
```
#### MainActivity.java
```
package com.example.check;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.CheckBox;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {
    private CheckBox chkMango, chkApple, chkGuava, chkGrape, chkBanana;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        chkMango = findViewById(R.id.chkMango);
        chkApple = findViewById(R.id.chkApple);
        chkGuava = findViewById(R.id.chkGuava);
        chkGrape = findViewById(R.id.chkGrape);
        chkBanana = findViewById(R.id.chkBanana);
    }
    public void showSelected(View view) {

        String selected = "You selected: \n";

        if(chkMango.isChecked())
            selected += "\nMango";

        if(chkApple.isChecked())
            selected += "\nApple";

        if(chkGuava.isChecked())
            selected += "\nGuava";

        if(chkGrape.isChecked())
            selected += "\nGrape";

        if(chkBanana.isChecked())
            selected += "\nBanana";

        Toast.makeText(MainActivity.this, selected, Toast.LENGTH_SHORT).show();
    }
}
```
#### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:gravity="center"
        android:text="Select your favorite place"
        style="@style/TextAppearance.AppCompat.Large"
        android:layout_margin="10dp"
        android:textStyle="bold"/>

    <CheckBox
        android:id="@+id/chkMango"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Mango"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkApple"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Apple"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkGuava"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Guava"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkGrape"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Grape"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkBanana"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Banana"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <Button android:id="@+id/btnDisplay"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Display"
        android:layout_marginTop="20dp"
        android:onClick="showSelected"/>

</LinearLayout>
```

## OUTPUT:

![fruit 1](https://user-images.githubusercontent.com/75235293/173176670-edc7f22e-eb45-4633-b62f-28351125cacd.jpeg)
![fruit 2](https://user-images.githubusercontent.com/75235293/173176682-4b674819-c524-4c43-9de2-a1e6f455c39d.jpeg)


## RESULT:
Thus a Simple Android Application to create a list using checkbox to display selected checkbox using Android Studio is developed and executed successfully.
