
# Ex.No:12 Design an application that draws basic graphical primitives on the screen.


## AIM:

To create and design an android application that draws basic graphical primitives on the screen using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “graphical″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Draw basic object details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to create and design an android application that draws basic graphical primitives on the screen.
Developed by: KEERTHY S.
Registeration Number : 212221040082.
*/
```
### MainActivity.java
```
package com.example.graphics;

import androidx.appcompat.app.AppCompatActivity;

import android.graphics.Bitmap;
import android.graphics.Canvas;
import android.graphics.Color;
import android.graphics.Paint;
import android.graphics.drawable.BitmapDrawable;
import android.os.Bundle;
import android.widget.ImageView;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Bitmap bg = Bitmap.createBitmap(720, 1280,
                Bitmap.Config.ARGB_8888);
        ImageView i = (ImageView) findViewById(R.id.ImageView);
        i.setBackgroundDrawable(new BitmapDrawable(bg));
        Canvas canvas = new Canvas(bg);
        Paint paint = new Paint();
        paint.setColor(Color.BLUE);
        paint.setTextSize(50);
        canvas.drawText("Rectangle", 420, 150, paint);
        canvas.drawRect(400, 200, 650, 700, paint);
        canvas.drawText("Circle", 120, 150, paint);
        canvas.drawCircle(200, 350, 150, paint);
        canvas.drawText("Square", 120, 800, paint);
        canvas.drawRect(50, 850, 350, 1150, paint);
        canvas.drawText("Line", 480, 800, paint);
        canvas.drawLine(520, 850, 520, 1150, paint);

    }
}
```
### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout android:layout_height="match_parent"
    android:layout_width="match_parent"
    xmlns:android="http://schemas.android.com/apk/res/android">
    <ImageView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:id="@+id/ImageView"/>
</RelativeLayout>
```

## OUTPUT

![Screenshot 2024-04-27 142053](https://github.com/keerthysesha/graphicsinandroid/assets/125575936/92970d50-eca3-41c8-9f86-f9919704d15f)

![Screenshot 2024-04-27 142115](https://github.com/keerthysesha/graphicsinandroid/assets/125575936/5ca88e9b-438a-4964-831b-0d1a3795c6b5)



## RESULT
Thus a Simple Android Application to create and design an android application that draws basic graphical primitives on the screen using Android Studio is developed and executed successfully.
