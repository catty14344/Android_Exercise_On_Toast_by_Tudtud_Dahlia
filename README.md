# Android_Exercise_On_Toast_by_Tudtud_Dahlia

<RelativeLayout 

xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools" 

android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Short Toast"
        android:onClick="ShortToast"
        android:id="@+id/button"
        android:layout_centerVertical="true"
        android:layout_alignParentRight="true"
        android:layout_alignParentEnd="true"
        android:layout_marginRight="56dp"
        android:layout_marginEnd="56dp" />
    <Button
        android:layout_marginEnd="44dp"
        android:layout_marginRight="44dp"
        android:layout_toStartOf="@+id/button"
        android:layout_toLeftOf="@+id/button"
        android:layout_alignTop="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/button1"
        android:text=" Long Toast"
        android:onClick="LongToast"/>
</RelativeLayout>

package com.example.user.myapplication;
import android.support.v7.app.ActionBarActivity;
import android.os.Bundle;
import android.view.Gravity;
import android.view.View
import android.view.Menu;
import android.view.MenuItem;
import android.widget.Toast;

public class MainActivity extends ActionBarActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
    public void LongToast(View view){
        Toast toast= Toast.makeText(this, "This is long", 

Toast.LENGTH_LONG);
        toast.setGravity(Gravity.BOTTOM,0,0);
        toast.show();
    }
    public void ShortToast(View view){
        Toast toast= Toast.makeText(this, "This is short", 

Toast.LENGTH_LONG);
        toast.setGravity(Gravity.BOTTOM,0,0);
        toast.show();
    }
}
