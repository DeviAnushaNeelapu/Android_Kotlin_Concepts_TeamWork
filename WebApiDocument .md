![web](https://user-images.githubusercontent.com/46557268/139213490-a14cc84d-6657-46f0-87b6-c0cf99119e38.JPG)

Web API creates an Interface through which any platform based device can communicate. Using HTTPClient API can be consumed for the operation for different devices.

Types of API
SOAP  : SOAP API does the communication using XML style. Which is heavy in architecture.
REST:  It’s one of the popular API and perfect for smaller devices. Communication made using JSON. 

# Web API Creation
	There are many languages which supports to write WEB API.
C#
JAVA
PHP
PYTHON
JavaScript( Node JS)


### Type of OPeration
### HTTPGet	:	Get Records single/multi
### HTTPPost	:	Add Record
###  HTTPPut	: 	Update Record based on ID
### HTTPDelete	: 	Delete Record based on ID




# Android Volley
Volley library introduced to work network based operation.


Demo: Create a project to work with Web API

Create a project named “Web-API-Demo”
Add the volley library.
Check for GradleScripts
Select build.gradle(Module: ProjectName.app)
Check for dependencies tag.
Add below of line
Implementation "com.android.volley:volley:1.2.0"

Click on Sync Now to make the changes.


## MainActivity.kt
```
class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
    }


    override fun onResume() {
        super.onResume()

        //1: Create volley object
        val queue = Volley.newRequestQueue(this)
        val fetchURL = "https://jsonplaceholder.typicode.com/posts"

        //2: Create a String Request to connect with API and fetch data and provide response as string
        val fetchRequest = StringRequest(Request.Method.GET,fetchURL,
                Response.Listener<String> {response ->
                    Log.d("Response",response.toString())
                },
                Response.ErrorListener {error ->
                    Log.d("Response Error",error.toString())
                })

        //3: Add the request inside volley object
        queue.add(fetchRequest)
    }
}

```
Add Internet Permission for the application
manifest> Android Manifest.xml
Add the below line just before the <application> tag.

    <uses-permission android:name="android.permission.INTERNET"/>



Display the Data Inside Recycler View.
```
Update the activity_main.xml file
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="16dp"
        android:layout_marginLeft="16dp"
        android:layout_marginTop="16dp"
        android:layout_marginEnd="16dp"
        android:layout_marginRight="16dp"
        android:text="REST API DATA"
        android:textColor="@color/black"
        android:textSize="24sp"
        android:textStyle="bold"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <androidx.recyclerview.widget.RecyclerView
        android:id="@+id/myRecycler"
        android:layout_width="0dp"
        android:layout_height="0dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:layout_marginBottom="8dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
  
Create a layout for recycler View row.
Right Click > layout> Android layout > “recycler_row”
```
  <?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="wrap_content">

    <TextView
        android:id="@+id/textView2"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="8dp"
        android:text="ID:"
        android:textColor="@color/black"
        android:textSize="18sp"
        android:textStyle="bold"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView3"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="16dp"
        android:text="USER ID:"
        android:textColor="@color/black"
        android:textSize="18sp"
        android:textStyle="bold"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView2" />

    <TextView
        android:id="@+id/textView4"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="16dp"
        android:text="Title:"
        android:textColor="@color/black"
        android:textSize="18sp"
        android:textStyle="bold"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView3" />

    <TextView
        android:id="@+id/textView5"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="16dp"
        android:layout_marginBottom="16dp"
        android:text="Body:"
        android:textColor="@color/black"
        android:textSize="18sp"
        android:textStyle="bold"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView4" />

    <TextView
        android:id="@+id/idTV"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="24dp"
        android:layout_marginLeft="24dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="24dp"
        android:layout_marginRight="24dp"
        android:text="TextView"
        android:textSize="18sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toEndOf="@+id/textView2"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/userTV"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="24dp"
        android:layout_marginLeft="24dp"
        android:layout_marginTop="16dp"
        android:layout_marginEnd="24dp"
        android:layout_marginRight="24dp"
        android:text="TextView"
        android:textSize="18sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toEndOf="@+id/textView3"
        app:layout_constraintTop_toBottomOf="@+id/idTV" />

    <TextView
        android:id="@+id/titleTV"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="24dp"
        android:layout_marginLeft="24dp"
        android:layout_marginTop="16dp"
        android:layout_marginEnd="24dp"
        android:layout_marginRight="24dp"
        android:text="TextView"
        android:textSize="18sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toEndOf="@+id/textView4"
        app:layout_constraintTop_toBottomOf="@+id/userTV" />

    <TextView
        android:id="@+id/bodyTV"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="24dp"
        android:layout_marginLeft="24dp"
        android:layout_marginTop="16dp"
        android:layout_marginEnd="24dp"
        android:layout_marginRight="24dp"
        android:layout_marginBottom="16dp"
        android:text="TextView"
        android:textSize="18sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toEndOf="@+id/textView5"
        app:layout_constraintTop_toBottomOf="@+id/titleTV" />
</androidx.constraintlayout.widget.ConstraintLayout>

```
  ```
Update the MainActivity.kt.


class MainActivity : AppCompatActivity() {
    var recyclerView: RecyclerView?=null
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        recyclerView = findViewById(R.id.myRecycler)
    }



    override fun onResume() {
        super.onResume()

        //1: Create volley object
        val queue = Volley.newRequestQueue(this)
        val fetchURL = "https://jsonplaceholder.typicode.com/posts"

        //2: Create a String Request to connect with API and fetch data and provide response as string
        val fetchRequest = StringRequest(Request.Method.GET,fetchURL,
                Response.Listener<String> {response ->

                    //Update Recycler View Adapter to display data as List
                    try{
                        val jsonArray = JSONArray(response)
                        val adapter = MyAdapter(jsonArray)

                        recyclerView!!.adapter = adapter
                        recyclerView!!.layoutManager = LinearLayoutManager(this)
                        recyclerView!!.addItemDecoration(DividerItemDecoration(this,DividerItemDecoration.VERTICAL))

                    }catch (e:Exception){
                        e.printStackTrace()
                    }



                },
                Response.ErrorListener {error ->
                    Log.d("Response Error",error.toString())
                })

        //3: Add the request inside volley object
        queue.add(fetchRequest)
    }
}
```
  ```

Create Recycler View Adapter
Right Click on java: Package> new > kotlin class : MyAdapter


class MyAdapter(jsonArray: JSONArray) : RecyclerView.Adapter<MyAdapter.ViewHolder>() {

    var recivedArray : JSONArray?= null
    init {
        recivedArray = jsonArray
    }



    //1: Link UI components for Recycler Row
    class ViewHolder(itemView: View) : RecyclerView.ViewHolder(itemView) {
        var userTXTV : TextView
        var idTXTV: TextView
        var titleTXTV:TextView
        var bodyTXTV:TextView


        init {
            userTXTV = itemView.findViewById(R.id.userTV)
            idTXTV = itemView.findViewById(R.id.idTV)
            titleTXTV = itemView.findViewById(R.id.titleTV)
            bodyTXTV = itemView.findViewById(R.id.bodyTV)

        }

    }

    //2:Link Recycler Row layout
    override fun onCreateViewHolder(parent: ViewGroup, viewType: Int): MyAdapter.ViewHolder {
        val recycler_row_view = LayoutInflater.from(parent.context).inflate(R.layout.recycler_row,parent,false)
        return ViewHolder(recycler_row_view)
    }

    //3: Link Data for Recycler Row UI Component
    override fun onBindViewHolder(holder: MyAdapter.ViewHolder, position: Int) {

        var jsonObject : JSONObject = recivedArray!!.getJSONObject(position)

        holder.idTXTV.text = jsonObject.getString("id")
        holder.userTXTV.text = jsonObject.getString("userId")
        holder.titleTXTV.text= jsonObject.getString("title")
        holder.bodyTXTV.text = jsonObject.getString("body")

    }

    //4: Size of Data
    override fun getItemCount(): Int {
        return recivedArray!!.length()
    }
}

```
