# Ex.No:2a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
```
1.
Design Layout: Create a UI in XML with an EditText for URL input and a Button to trigger the action.
2.
Initialize Views: In the Activity, link the XML components to Java objects using findViewById().
3.
Handle Click Event: Set an OnClickListener on the button to capture the text entered by the user.
4.
Create Implicit Intent: Define an Intent using ACTION_VIEW and parse the input string into a Uri.
5.
Launch Activity: Call startActivity() to prompt the system to open the URL in a web browser.
```

## PROGRAM:

```
Program to print the text “Implicitintent”.
Developed by: SANJAY K
Registeration Number : 212223220094
MainActivity.java
```
```
package com.example.implicit;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        EditText editText;
        Button button;

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.button);
        editText = findViewById(R.id.editTextText);

        button.setOnClickListener(view -> {
            String url=editText.getText().toString();
            Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
            startActivity(intent);
        });
    }
}
```
### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginEnd="88dp"
        android:text="Implicit Intent"
        android:textSize="34sp"
        app:layout_constraintBottom_toTopOf="@+id/editTextText"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.879"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.5" />

    <EditText
        android:id="@+id/editTextText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginEnd="76dp"
        android:ems="10"
        android:inputType="text"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.816"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView"
        app:layout_constraintVertical_bias="0.5" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginEnd="144dp"
        android:text="Click"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.899"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editTextText"
        app:layout_constraintVertical_bias="0.493" />
</androidx.constraintlayout.widget.ConstraintLayout>
```

## OUTPUT

### activity_main.xml
<img width="1920" height="1080" alt="Screenshot (243)" src="https://github.com/user-attachments/assets/a8cd6d5f-1321-4449-8abd-e00796c483b7" />

### MainActivity.java
<img width="1920" height="1080" alt="Screenshot (239)" src="https://github.com/user-attachments/assets/c662813a-8649-40d3-9c4a-aa91f23853d7" />

### Implicit Intent
<img width="1920" height="1080" alt="Screenshot (240)" src="https://github.com/user-attachments/assets/d3e6fe80-75c2-4188-afb0-66c6e9467f15" />

### Navigated to URL
<img width="1920" height="1080" alt="Screenshot (242)" src="https://github.com/user-attachments/assets/e892b518-ed9b-43b1-bd3f-1060fd4245d5" />






## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


