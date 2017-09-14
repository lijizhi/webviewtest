# webviewtest
完成一个简单的网络加载，只需要以下三步：

*    新建一个WebviewTest项目，修改activity_main.xml中的代码如下所示：
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent" >

    <WebView
        android:id="@+id/web_view"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />

</LinearLayout>

*    然后修改MainActyivity中的代码，如下所示：


    public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
      
      super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        WebView webView = (WebView) findViewById(R.id.web_view);
        webView.getSettings().setJavaScriptEnabled(true);
        webView.setWebViewClient(new WebViewClient());
        webView.loadUrl("http://www.baidu.com");
      }

    }


*      最后一步就是添加需要的权限，修改AndroidManifest.xml文件，并加入如下权限声明，如下所示：

      uses-permission android:name="android.permission.INTERNET" 

  
