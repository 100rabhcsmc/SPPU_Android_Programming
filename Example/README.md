**Example 1. using the spinnerview to display one item at a time in android**
MainActivity.java:

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view. View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.Spinner;
import android.widget.Toast;
public class MainActivity extends AppCompatActivity{
String[Ipresidents;
\*\* Called when the actllty is 1rst created.

@override
bublic void oncreate(Bundle savedinstancestate)
{ super. oncreate(savedInstanceState);
setContentView(R.layout.activity_main);
presidents = getResources().getStringArray
(R.array.presidents_array);
Spinner s1 = (Spinner) findViewById(R.id.spinner1);
ArrayAdapter‹String› adapter = newArrayAdapter<String>(this,
android.R.layout.simple_spinner_item, presidents);
51.setAdapter (adapter);
s1.setOnItemSelectedListener(newAdapterView.OnItemSelectedListene
@override
public void onItemSelected (AdapterView<?> argo,
View arel, int arg2, long arg3)
it index = arg@.getSelectedItemPosition();
Toast.makeText (getBaseContext (),
"You have selected item:" + presidents index,
Toast. LENGTH_SHORT) . show();
@override
public void onNothingSelected (AdapterView<?> argo){}
});
}
}

**Example 2 : Displaying a LongList of Items Using the List View.**

MainActivity.java

import android.app.ListActivity;
import android.os.Bundle;
import android. view. view:
import android.widget.ArrayAdapter;
import android.widget.ListView;
import android.widget. Toast;
public class MainActivity extends ListActivitvf
String presidents =
"Dwight D. Eisenhower'
"John F. Kennedy"
"Lundon B. Johnson"
"Richard Nixon"
"Gerald Ford"
"Jimmy Carter
"Ronald Reagan"
"George H. W. Bush"
"Bill Clinton",
"George W. Bush"
"Barack Obama"
@override
public void onCreate (Bundle savedInstanceState)
super.onCreate(savedInstanceState);
setListAdapter(newArrayAdapter<String>(this,
android.R.layout.simple list item 1,
presidents));
bublic vol onlistitemcIick(
ListView parent, View, int position, long id'
Toast.makeText (this,
"You have selected" + presidents[position],
Toast. LENGTH_SHORT) . show();
}
}
