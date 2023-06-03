# Ex.No:8 To create a gallery control using android studio to display images or photos.


## AIM:

To create a gallery control using android studio to display images or photos.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
 Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “gallerycontrol″ and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Get images details and Add images in MainActivity file.

Step 7: Save and run the application.


## PROGRAM:
```
/*
Program to print the text “GalleryControl”.
Developed by: SATHYA N
Registeration Number :212221040149
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
             <ImageView
                 android:id="@+id/imageView"
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:layout_marginTop="36dp"
                 app:layout_constraintBottom_toTopOf="@+id/languagesGallery"
                 app:layout_constraintEnd_toEndOf="parent"
                 app:layout_constraintHorizontal_bias="0.466"
                 app:layout_constraintStart_toStartOf="parent"
                 app:layout_constraintTop_toTopOf="parent"
                 tools:srcCompat="@tools:sample/avatars" />
             <Gallery
                 android:id="@+id/languagesGallery"
                 android:layout_width="match_parent"
                 android:layout_height="wrap_content"
                 android:animationDuration="2000"
                 android:padding="10dp"
                 android:spacing="5dp"
                 android:unselectedAlpha="50"
                 app:layout_constraintBottom_toBottomOf="parent"
                 app:layout_constraintEnd_toEndOf="parent"
                 app:layout_constraintHorizontal_bias="0.0"
                 app:layout_constraintStart_toStartOf="parent"
                 app:layout_constraintTop_toTopOf="parent"></Gallery>
             </androidx.constraintlayout.widget.ConstraintLayout>
             
## MainActivity.java
              package com.example.galleryview;
              import androidx.appcompat.app.AppCompatActivity;
              import android.os.Bundle;
              import android.view.View;
              import android.widget.AdapterView;
              import android.widget.Gallery;
              import android.widget.ImageView;
              public class MainActivity extends AppCompatActivity {
              Gallery simpleGallery;
              CustomizedGalleryAdapter customGalleryAdapter;
              ImageView selectedImageView;
              int[] images = {R.drawable.p1, R.drawable.p2,R.drawable.p3,R.drawable.p4};
              @Override
              protected void onCreate(Bundle savedInstanceState) {
                  super.onCreate(savedInstanceState);
                  setContentView(R.layout.activity_main);
                  simpleGallery = (Gallery) findViewById(R.id.languagesGallery);
                  selectedImageView = (ImageView) findViewById(R.id.imageView);
                  customGalleryAdapter = new CustomizedGalleryAdapter(getApplicationContext(), images);
                  simpleGallery.setAdapter(customGalleryAdapter);
                  simpleGallery.setOnItemClickListener(new AdapterView.OnItemClickListener() {
                     @Override
                     public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
                        selectedImageView.setImageResource(images[position]);
                        }
                      });
                    }
                  }


## CustomizedGalleryAdapter
              package com.example.galleryview;
              import android.content.Context;
              import android.view.View;
              import android.view.ViewGroup;
              import android.widget.BaseAdapter;
              import android.widget.Gallery;
              import android.widget.ImageView;
              public class CustomizedGalleryAdapter extends BaseAdapter {
              private Context context;
              private int[] images;
              public CustomizedGalleryAdapter(Context c, int[] images) {
                 context = c;
                 this.images = images;
              }
              public int getCount() {
                 return images.length;
              }
              public Object getItem(int position) {
                 return position;
              }
              public long getItemId(int position) {
                 return position;
              }
              public View getView(int position, View convertView, ViewGroup parent) {
                 ImageView imageView = new ImageView(context);
                 imageView.setImageResource(images[position]);
                 imageView.setLayoutParams(new Gallery.LayoutParams(200, 200));
                 return imageView;
                }
              }
## OUTPUT
![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/a097e955-fc1f-43d5-9edd-dc9a3d9b0d51)

![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/fec0f187-233a-470c-97c8-53af9358d1b5)

![image](https://github.com/Sathya-006/Mobile-Application-Development/assets/121661327/2c8ca49b-d1bf-46e3-a01d-351b1ea20d77)




## RESULT
Thus a Simple Android Application to create a gallery control using android studio to display images or photos is developed and executed successfully.


