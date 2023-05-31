# Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.


## AIM:

To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “Hello World”.
Developed by: SATHYA N
Registeration Number : 212221040149
*/
```
## activity_main.xml
              <?xml version="1.0" encoding="utf-8"?>
              <androidx.constraintlayout.widget.ConstraintLayout 
                   xmlns:android="http://schemas.android.com/apk/res/android"
                   xmlns:app="http://schemas.android.com/apk/res-auto"
                   xmlns:tools="http://schemas.android.com/tools"
                   android:layout_width="match_parent"
                   android:layout_height="match_parent"
                   tools:context=".MainActivity">
               <TextView
                   android:layout_width="238dp"
                   android:layout_height="105dp"
                   android:text="Hello World!"
                   android:textSize="100px"
                   android:textStyle="italic"
                   app:layout_constraintBottom_toBottomOf="parent"
                   app:layout_constraintEnd_toEndOf="parent"
                   app:layout_constraintHorizontal_bias="0.591"
                   app:layout_constraintStart_toStartOf="parent"
                   app:layout_constraintTop_toTopOf="parent"
                   app:layout_constraintVertical_bias="0.499" />
               </androidx.constraintlayout.widget.ConstraintLayout>
               
## MainActivity.java
               package com.example.helloworld;
               import androidx.appcompat.app.AppCompatActivity;
               import android.os.Bundle;
               import android.util.Log;
               import android.widget.Toast;
               public class MainActivity extends AppCompatActivity {
                private static final String TAG = "HelloWorldActivity";
                @Override
                protected void onCreate(Bundle savedInstanceState) {
                    super.onCreate(savedInstanceState);
                    setContentView(R.layout.activity_main);
                    Log.d(TAG, "onCreate: ");
                    Toast.makeText(this, "onCreate", Toast.LENGTH_SHORT).show();
                    }
                @Override
                protected void onStart() {
                    super.onStart();
                    Log.d(TAG, "onStart: ");
                    Toast.makeText(this, "onStart", Toast.LENGTH_SHORT).show();
                    }
                @Override
                protected void onResume() {
                    super.onResume();
                    Log.d(TAG, "onResume: ");
                    Toast.makeText(this, "onResume", Toast.LENGTH_SHORT).show();
                    }
                @Override
                protected void onPause() {
                    super.onPause();
                    Log.d(TAG, "onPause: ");
                    Toast.makeText(this, "onPause", Toast.LENGTH_SHORT).show();
                    }
                @Override
                protected void onStop() {
                    super.onStop();
                    Log.d(TAG, "onStop: ");
                    Toast.makeText(this, "onStop", Toast.LENGTH_SHORT).show();
                    }
                @Override
                protected void onDestroy() {
                    super.onDestroy();
                    Log.d(TAG, "onDestroy: ");
                    Toast.makeText(this, "onDestroy", Toast.LENGTH_SHORT).show();
                    }
                @Override
                protected void onRestart() {
                    super.onRestart();
                    Log.d(TAG, "onRestart: ");
                    Toast.makeText(this, "onRestart", Toast.LENGTH_SHORT).show();
                    }
                    }

## OUTPUT
![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/02f3fc11-fc2d-4af2-ad45-fb0e1434dcab)
![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/a103fb78-20d4-4688-ad22-27dbb96bb6d6)
![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/c7f30f59-8de5-43dc-8c4f-dcb7b0a83dcb)
![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/4ed4b3f4-1e99-4e29-8aa2-8b286e92ae3d)
![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/f73cac24-3f09-4905-9ca2-ebc6633bf20c)
![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/511c30c0-4d09-4aaf-9022-80b174b5155e)
![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/da329625-4863-4009-894e-a33e9f1a77d9)




## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
