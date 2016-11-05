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
```
import android.context.Context;
import android.database.sqlite.SQLiteDatabase;
import android.database.sqlite.SQLiteOpenHelper;
public class DBHelper extends SQLiteOperator{
  
}
```
