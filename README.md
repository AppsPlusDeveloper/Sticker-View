<center></br><b>Intent-Filter</b> es un sistema de Android para recibir contenido de otras Apps como enlaces o archivos, en este proyecto te muestro a implementarlo y usarlo correctamente.
    </br> </br>
    <img src="./Preview/logo.png" width=150 title="Screen">
</center></br>

## Importación

Importa el archivo java "StickerView" a tú proyecto y añade iconos con los nombres "R.drawable.crop_black", "R.drawable.close", "R.drawable.rotate_cw_black". Estos iconos serán los que tendra tú Sticker View.

## Inicio

Comencemos por declarar una ID a nuestro Sticker View.

```java
private StickerView st;
```

Ahora seleccionemos un FrameLayout sobre el cuál pondremos nuestro StickerView.

```java
myframe.addView(st);
```

Para seleccionar una view.

```java
st.select(myview);
```

Quitar la selección actual.

```java
st.unselect();
```

## Eventos

Los eventos disponibles son los siguentes:

```java
st.setOnEvent(new StickerView.onEvent(){
@Override 
public void onSizeChanged(int height,int width){

}
@Override 
public void onClose(){

}
@Override
public void onRotation(float rotation){

}

});
```

## Ejemplo De Diseño

El FrameLayout debe contener dentro las Views que quieras usar como Stickers.

```xml
<FrameLayout
 android:id="@+id/myframe"
 android:layout_width="match_parent"
 android:layout_height="match_parent" android:gravity="center_horizontal|center_vertical"
 android:orientation="vertical">
   <ImageView
   android:id="@+id/myview"
   android:layout_width="wrap_content"
   android:layout_height="wrap_content"
   android:src="@drawable/default_image"
   android:scaleType="fitCenter" />
</FrameLayout>
```
