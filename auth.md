# Authentication Module

- kütüphane olarak ekleme         `import { getAuth } from "firebase/auth";` 

- initilization etme ve referansını alma    `const auth = getAuth(app);`

- email ve sifre ile kullanici ekleme, promise döndürür `createUserWithEmailAndPassword(auth, email, password)`

- islemin bitmesini bekler ve eger basarili olursa `.then((userCredential) => { const user = userCredential.user; })`

- islemin bitmesini bekler ve eger hata olusursa `.catch((error) => { const errorCode = error.code; const errorMessage = error.message; });`

- olan kullanicinin credential bilgilerini alma `signInWithEmailAndPassword(auth, email, password) .then((userCredential) ...)`

- kullanıcı giriş veya çıkış yapma eventini takip eder eğer user null değilse mevcutta giriş yapmış biri vardır `onAuthStateChanged(auth, (user) => { if(user) ... else ... }`

- güncel kullanıcıyı getirir `var guncel_kullanici = auth.currentUser`

- profili update etme `updateProfile(auth.currentUser, {displayName: name, photoUrl = url })`
