package com.example.androidhw2;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final Intent i = new Intent(MainActivity.this, MainActivity2.class);
        EditText name = findViewById(R.id.yourname);
        EditText age = findViewById(R.id.yourage);
        EditText job = findViewById(R.id.yourjob);
        EditText phone = findViewById(R.id.phonenumber);
        EditText email = findViewById(R.id.youremail);
        Button next = findViewById(R.id.button);
        next.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String info = name.getText().toString();
                String age1 = age.getText().toString();
                String job1 = job.getText().toString();
                String phone1 = phone.getText().toString();
                String email1 = email.getText().toString();
                i.putExtra("info1", info);
                i.putExtra("age2", age1);
                i.putExtra("job2", job1);
                i.putExtra("phone2", phone1);
                i.putExtra("email2", email1);
                startActivity(i);
            }
        });
    }
}