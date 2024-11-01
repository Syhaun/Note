```java
new Thread(new Runnable() {
@Override
 public void run() { 
 try { 
Thread.sleep(3000);
//界面跳转代码
Intent intent =new Intent(WelcomeActivity.this, MainActicity.class);
 startActivity(intent); 
 } catch (InterruptedException e) { 
 e.printStackTrace(); 
 } 
 } 
 }).start(); 
```