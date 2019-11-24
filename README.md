# anim-press-view
Easy to use Push/Pop animation effect on view click 

#### build.gradle
Add below codes to your root `build.gradle` file (not your module build.gradle file).
```gradle
repositories {
    maven { url 'https://jitpack.io' }
}

dependencies {
    implementation 'com.github.saurabhdhillon:anim-press-view:0.0.1'
}
```

### PressEffectButton
```gradle
<com.animation.animpresseffect.PressEffectButton
        android:id="@+id/button"
        android:layout_width="match_parent"
        android:layout_height="50dp"
        android:layout_margin="10dp"
        android:background="@color/colorPrimary"
        android:text="Button"
        android:textColor="@android:color/white"
        app:button_duration="800"
        app:button_scale="0.9"
        app:layout_constraintBottom_toTopOf="@id/card"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
```

### PressEffectCardView
```gradle
 <com.animation.animpresseffect.PressEffectCardView
        android:id="@+id/card"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="16dp"
        app:button_duration="600"
        app:button_scale="0.7"
        app:cardElevation="6dp"
        app:layout_constraintBottom_toTopOf="@+id/container"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="center"
            android:layout_margin="16dp"
            android:text="Card View"
            android:textColor="#000000"
            android:textSize="20dp" />

    </com.animation.animpresseffect.PressEffectCardView>
```

### PressAnimContainerLayout
PressEffectContainerLayout gives push/pop click effect to all child views.

```gradle
<com.animation.animpresseffect.PressEffectContainerLayout
        android:id="@+id/container"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="16dp"
        app:button_duration="500"
        app:button_scale="0.5"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/card">

        <androidx.appcompat.widget.LinearLayoutCompat
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginStart="16dp"
            android:layout_marginEnd="16dp"
            android:background="@color/colorPrimaryDark"
            android:orientation="vertical">

            <TextView
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_gravity="end"
                android:layout_marginTop="16dp"
                android:layout_marginEnd="16dp"
                android:text="Text View 1"
                android:textColor="#ffffff"
                android:textSize="16dp" />

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_marginStart="16dp"
                android:layout_marginTop="16dp"
                android:layout_marginBottom="16dp"
                android:text="Text View 2"
                android:textColor="#ffffff"
                android:textSize="16dp" />

        </androidx.appcompat.widget.LinearLayoutCompat>

    </com.animation.animpresseffect.PressEffectContainerLayout>
```
