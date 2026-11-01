# Ronbu
Ön ve arka kameraların eş zamanlı ekranda izlenmesi
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#000000"
    android:orientation="vertical">

    <!-- 1. ÜST PANEL: ARKA KAMERA CANLI YAYINI -->
    <FrameLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1">

        <androidx.camera.view.PreviewView
            android:id="@+id/viewFinderBack"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            app:scaleType="fillCenter" />

        <!-- Canlı Etiketi -->
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="top|start"
            android:layout_margin="16dp"
            android:background="#99000000"
            android:paddingHorizontal="10dp"
            android:paddingVertical="4dp"
            android:text="🔴 CANLI - ARKA KAMERA"
            android:textColor="#00FF66"
            android:textSize="12sp"
            android:textStyle="bold" />
    </FrameLayout>

    <!-- Ayırıcı Çizgi -->
    <View
        android:layout_width="match_parent"
        android:layout_height="3dp"
        android:background="#333333" />

    <!-- 2. ALT PANEL: ÖN KAMERA CANLI YAYINI -->
    <FrameLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1">

        <androidx.camera.view.PreviewView
            android:id="@+id/viewFinderFront"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            app:scaleType="fillCenter" />

        <!-- Canlı Etiketi -->
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="top|start"
            android:layout_margin="16dp"
            android:background="#99000000"
            android:paddingHorizontal="10dp"
            android:paddingVertical="4dp"
            android:text="🔴 CANLI - ÖN KAMERA"
            android:textColor="#00FF66"
            android:textSize="12sp"
            android:textStyle="bold" />
    </FrameLayout>

</LinearLayout>
