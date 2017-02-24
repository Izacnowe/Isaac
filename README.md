# Isaac
MY HEALTH PLATFORM APPLICATION CODE
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/izac_page1"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context="izaac.myown.Page1">

    <Button
        android:text="Sign in"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/button"
        android:background="@android:drawable/ic_partial_secure"
        android:onClick="ask"
        android:layout_marginTop="51dp"
        android:layout_below="@+id/editText3"
        />

    <Button
        android:text="Create account"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/button2"
        android:onClick="register"
        android:layout_alignBaseline="@+id/button"
        android:layout_alignBottom="@+id/button"
        android:layout_toEndOf="@+id/button"
        android:layout_marginStart="54dp" />

    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:inputType="textPassword"
        android:ems="10"
        android:id="@+id/editText3"
        android:hint="enter password"
        android:textAlignment="center"
        android:layout_centerVertical="true"
        android:layout_alignParentStart="true" />

    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:inputType="textPersonName"
        android:text="enter your email"
        android:ems="10"
        android:layout_marginBottom="18dp"
        android:id="@+id/editText2"
        android:textAlignment="center"
        android:hint="enter Email"
        android:layout_above="@+id/editText3"
        android:layout_alignParentStart="true" />

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Who are you?"
        android:background="@android:drawable/ic_menu_help"
        android:textAlignment="center"
        android:textColor="@android:color/holo_red_dark"
        android:textSize="24sp"
        style="@android:style/Widget.DeviceDefault.Light.TextView.SpinnerItem"
        android:layout_below="@+id/editText"
        android:layout_alignParentStart="true" />

    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:inputType="textPersonName"
        android:text="username"
        android:ems="10"
        android:id="@+id/editText9"
        android:textAlignment="center"
        android:layout_above="@+id/editText2"
        android:layout_alignParentStart="true" />
</RelativeLayout>


package izaac.myown;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;

public class Page1 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.izac_page1);
    }

    public void ask(View view) {
        Intent intent = new Intent (Page1.this, Page2.class);
        startActivity(intent);
    }

    public void register(View view) {
        Intent intent = new Intent (Page1.this, Page3.class);
        startActivity(intent);
    }
}

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/izac_page2"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context="izaac.myown.Page2">

    <TextView
        android:text="Welcome to your doctor!!"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:id="@+id/textView2"
        android:textSize="30sp"
        android:textColor="@android:color/holo_green_dark"
        android:layout_alignParentTop="true"
        android:textAlignment="center"
        android:background="@android:drawable/star_big_on"
        android:textColorHighlight="?android:attr/colorMultiSelectHighlight"
        android:layout_alignParentStart="true" />

    <Button
        android:text="ask me"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/ask"
        android:textColor="@color/colorPrimary"
        android:textSize="24sp"
        android:layout_marginBottom="93dp"
        android:layout_alignParentBottom="true"
        android:layout_alignParentStart="true" />

    <Button
        android:text="SIGNOUT"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/back"
        android:background="@android:drawable/ic_lock_lock"
        android:textSize="18sp"
        android:onClick="back"
        android:layout_marginEnd="36dp"
        android:layout_alignTop="@+id/ask"
        android:layout_alignParentEnd="true" />

    <TextView
        android:text="Any health question??"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="20dp"
        android:id="@+id/textView3"
        android:textSize="24sp"
        android:layout_below="@+id/textView2"
        android:layout_centerHorizontal="true" />

    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:inputType="textPersonName"
        android:text=" "
        android:ems="10"
        android:id="@+id/question"
        android:textSize="24sp"
        android:textAlignment="center"
        android:cursorVisible="true"
        android:layout_below="@+id/textView3"
        android:layout_alignParentStart="true"
        android:layout_marginTop="24dp"
        android:hint="ask a question" />
</RelativeLayout>

package izaac.myown;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;

public class Page2 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.izac_page2);
    }

    public void back(View view) {
        Intent intent = new Intent (Page2.this, Page1.class);
        startActivity(intent);
    }
}

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/izac_page3"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context="izaac.myown.Page3">

    <TextView
        android:text="REGISTER"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/textView"
        android:textSize="24sp"
        android:layout_alignParentTop="true"
        android:layout_centerHorizontal="true"
        android:textColor="@android:color/holo_red_dark"
        android:background="@android:drawable/ic_input_add" />

    <Button
        android:text="close"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/exit"
        android:textSize="14sp"
        android:layout_alignBaseline="@+id/button3"
        android:layout_alignBottom="@+id/button3"
        android:layout_alignParentEnd="true" />

    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:inputType="textEmailAddress"
        android:ems="10"
        android:layout_below="@+id/editText4"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="16dp"
        android:id="@+id/editText10"
        android:textAlignment="center"
        android:hint="enter your Email" />

    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:inputType="textPassword"
        android:ems="10"
        android:layout_below="@+id/editText10"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="19dp"
        android:id="@+id/editText11"
        android:hint="create password"
        android:textAlignment="center" />

    <Button
        android:text="Register"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/button3"
        android:textSize="14sp"
        android:onClick="homepage"
        android:fontFamily="@android:string/dialog_alert_title"
        android:layout_below="@+id/editText11"
        android:layout_alignParentStart="true"
        android:layout_marginTop="71dp" />

    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:inputType="textPersonName"
        android:text="create username"
        android:ems="10"
        android:layout_marginTop="23dp"
        android:id="@+id/editText4"
        android:hint="create username"
        android:textAlignment="center"
        android:layout_below="@+id/textView"
        android:layout_alignParentStart="true" />

</RelativeLayout>

package izaac.myown;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;

public class Page3 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.izac_page3);
    }

    public void homepage(View view) {

        Intent intent = new Intent (Page3.this, Page1.class);
        startActivity(intent);
    }
 }
