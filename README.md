# laandroidappdevesstlcldatastor
```
public class DataItem{
  private String itemId;
  private String itemName;
  private String description;
  private String category;
  private int sortPosition;
  private double price;
  private String image;
}
```


##4. Manage Relational Data with SQLite
###1 SQLite and Android
classes
```
SQLiteClosable
SQLiteCursor
SQLiteDatabase
SQLiteOpenHelper
SQLiteProgram
SQLiteQuery
SQLiteQueryBundler
SQLiteStatement
```

###2 Create an SQLite database

####01:50
REAL = double in java
```
import android.context.Context;
import android.database.sqlite.SQLiteDatabase;
import android.database.sqlite.SQLiteOpenHelper;
public class DBHelper extends SQLiteOperator{
  public DBHelper(Context context,String name,SQLiteDatabase.CursorFactiry factory,int version){
    super(context,name,factory,version);
  }
}
```
then refactor (DBHelper.java)
```
public static final String DB_FILE_NAMW="test.db";
public static final int DB_VERSION = 1;
public DBHelper(Context context){
  super(context,DBFILE,null,DBVERSION);
}
```

####05:08
ItemTable.java
```
public class
```

####05:17

DBHelper.java
```
@Override
public void onCreate(SQLiteDatabase db){
  db.execSQL(ItemTable.SQL_CREATE)
}
```


###7 Filter and sort data
####01:10 DataSource.java
```
public List<DataItem> getAllItems(){
  List<DataItem> dataItems = new ArrayList<>();
  Cursor cursor = mDatabase.query(Itemtable.TABLE_ITEMS, ItemsTable.ALL_CLOUMNS, null,null,null,null,ItemTable.COLUMN_NAME);
  while(cursor.moveToNext()){
    DataItem item = new DataItem();
    item.setItemId(cursor.getString(cursor.getColumnIndex(ItemsTable.COLUMN_ID)));
    ...
    dataItems.add(item);
  }
  cursor.close();
  return dataItems;
}
```
