# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by: SATHYA N
Registeration Number : 212221040149
*/
```
## activity_main.xml 
                   <?xml version="1.0" encoding="utf-8"?>
                   <androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
                   xmlns:app="http://schemas.android.com/apk/res-auto"
                   xmlns:tools="http://schemas.android.com/tools"
                   android:layout_width="match_parent"
                   android:layout_height="match_parent"
                   tools:context=".MainActivity">

                  <EditText
                          android:id="@+id/numberEditText1"
                          android:layout_width="wrap_content"
                          android:layout_height="wrap_content"
                          android:layout_marginTop="172dp"
                          android:ems="10"
                          android:inputType="textPersonName"
                          android:text=""
                          app:layout_constraintEnd_toEndOf="parent"
                          app:layout_constraintHorizontal_bias="0.497"
                          app:layout_constraintStart_toStartOf="parent"
                          app:layout_constraintTop_toTopOf="parent" />

                 <Button
                          android:id="@+id/factorialButton"
                          android:layout_width="wrap_content"
                          android:layout_height="wrap_content"
                          android:layout_marginTop="340dp"
                          android:text="Button"
                          app:layout_constraintEnd_toEndOf="parent"
                          app:layout_constraintHorizontal_bias="0.498"
                          app:layout_constraintStart_toStartOf="parent"
                          app:layout_constraintTop_toTopOf="parent" />

                  </androidx.constraintlayout.widget.ConstraintLayout>

## MainActivity.java 
                  package com.example.factorialexplicit;
                  import static com.example.factorialexplicit.R.id.factorialButton;
                  import static com.example.factorialexplicit.R.id.numberEditText1;
                  import androidx.appcompat.app.AppCompatActivity;
                  import android.annotation.SuppressLint;
                  import android.content.Intent;
                  import android.os.Bundle;
                  import android.view.View;
                  import android.widget.Button;
                  import android.widget.EditText;
                  public class MainActivity extends AppCompatActivity {
                  private EditText numberEditText;
                  private Button factorialButton;
                   @Override
                  protected void onCreate(Bundle savedInstanceState) {
                  super.onCreate(savedInstanceState);
                  setContentView(R.layout.activity_main);
                  numberEditText = findViewById(R.id.numberEditText1);
                  factorialButton = findViewById(R.id.factorialButton);
                  factorialButton.setOnClickListener(new View.OnClickListener() {
                   @Override
                    public void onClick(View v) {
                  int number = Integer.parseInt(numberEditText.getText().toString());
                  Intent intent = new Intent(MainActivity.this, FactorialActivity.class);
                  intent.putExtra("number", number);
                  startActivity(intent);
                   }
                     });
                     }
                  }

## activity_main2.xml 
                   <?xml version="1.0" encoding="utf-8"?>
                   <androidx.constraintlayout.widget.ConstraintLayout 
                   xmlns:android="http://schemas.android.com/apk/res/android"
                   xmlns:app="http://schemas.android.com/apk/res-auto"
                   xmlns:tools="http://schemas.android.com/tools"
                   android:layout_width="match_parent"
                   android:layout_height="match_parent"
                   tools:context=".MainActivity">
                   <EditText
                            android:id="@+id/numberEditText1"
                            android:layout_width="wrap_content"
                            android:layout_height="wrap_content"
                            android:layout_marginTop="172dp"
                            android:ems="10"
                            android:inputType="textPersonName"
                            android:text=""
                            app:layout_constraintEnd_toEndOf="parent"
                            app:layout_constraintHorizontal_bias="0.497"
                            app:layout_constraintStart_toStartOf="parent"
                            app:layout_constraintTop_toTopOf="parent" />

                   <Button
                             android:id="@+id/factorialButton"
                             android:layout_width="wrap_content"
                             android:layout_height="wrap_content"
                             android:layout_marginTop="340dp"
                             android:text="Button"
                             app:layout_constraintEnd_toEndOf="parent"
                             app:layout_constraintHorizontal_bias="0.498"
                             app:layout_constraintStart_toStartOf="parent"
                             app:layout_constraintTop_toTopOf="parent" />

                    </androidx.constraintlayout.widget.ConstraintLayout>

## MainActivity2.java package com.example.explicitintent; 
                          package com.example.factorialexplicit;
                          import static com.example.factorialexplicit.R.id.factorialTextView;
                          import androidx.appcompat.app.AppCompatActivity;
                          import android.annotation.SuppressLint;
                          import android.content.Intent;
                          import android.os.Bundle;
                          import android.widget.TextView;
                          public class FactorialActivity extends AppCompatActivity {
                          private TextView factorialTextView;
                             @Override
                              protected void onCreate(Bundle savedInstanceState) {
                              super.onCreate(savedInstanceState);
                              setContentView(R.layout.activity_factorial);
                              factorialTextView = findViewById(R.id.factorialTextView;
                              Intent intent = getIntent();
                              int number = intent.getIntExtra("number", 0);
                              long factorial = calculateFactorial(number);
                              factorialTextView.setText("Factorial of " + number + " is " + factorial)
                              }
                              private long calculateFactorial(int number) {
                              long factorial = 1;
                              for (int i = 1; i <= number; i++) {
                              factorial *= i;
                              }
                              return factorial;
                              }
                              }


## OUTPUT

![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/0cd01c69-f549-46c3-82f0-ec7e419c99eb)
![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/b89281d4-ad93-43a2-8e4c-6099c3a74725)
![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/f7c95672-002c-478e-85c3-fb5e1f600eaf)
![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/10365dd0-bc73-43ce-bea5-d5e2d0049579)
![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/e187cdcb-93be-45fa-8e88-83483fe03d27)
![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/e7f26fe4-9b03-4ded-9758-465aa3c8057a)



## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


