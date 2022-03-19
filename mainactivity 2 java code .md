
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.TextView;

public class MainActivity2 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);
        TextView nameanswer = findViewById(R.id.name3);
        TextView ageanswer = findViewById(R.id.age3);
        TextView jobanswer = findViewById(R.id.job3);
        TextView phoneanswer = findViewById(R.id.phone3);
        TextView emailanswer = findViewById(R.id.email3);

        Bundle bundle = getIntent().getExtras();
        Bundle bundle1 = getIntent().getExtras();
        Bundle bundle2 = getIntent().getExtras();
        Bundle bundle3 = getIntent().getExtras();
        Bundle bundle4 = getIntent().getExtras();

        String info2 = bundle.getString("info1");
        String age4 = bundle.getString("age2");
        String job4 = bundle.getString("job2");
        String phone4 = bundle.getString("phone2");
        String email4 = bundle.getString("email2");


        nameanswer.setText(info2);
        ageanswer.setText(age4);
        jobanswer.setText(job4);
        phoneanswer.setText(phone4);
        emailanswer.setText(email4);
    }
}