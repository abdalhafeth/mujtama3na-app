`PKG: android.app
IMP: android.os.Bundle
IMP: android.view.View
IMP: android.widget.Button
IMP: android.widget.EditText
IMP: android.widget.Toast
IMP: com.google.firebase.auth.FirebaseAuth
CLS: MainActivity EXT android.app.AppCompatActivity {
  PRV mAuth: FirebaseAuth
  PUB onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState)
    setContentView(R.layout.activity_main)
  }
}
CLS: LoginActivity EXT android.app.AppCompatActivity {
  PRV email: EditText
  PRV password: EditText
  PRV loginBtn: Button
  PRV mAuth: FirebaseAuth
  PUB onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState)
    setContentView(R.layout.activity_login)
    email = findViewById(R.id.email)
    password = findViewById(R.id.password)
    loginBtn = findViewById(R.id.loginBtn)
    mAuth = FirebaseAuth.getInstance()
    loginBtn.setOnClickListener
