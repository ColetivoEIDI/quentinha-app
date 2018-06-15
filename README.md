# Quentinha App Mobile
## functionalities:
#### X Login
#### X Cadastro
#### X Registro de Preferências
#### X Lista de Usuários On
#### X Mudar para Off
#### X Convidar
#### X Listar Convites
#### X Aceitar
#### X Abrir Whatsapp/Telegram

## Installation:
<pre>
<code>
$ git clone https://github.com/ColetivoEIDI/quentinha-app.git
$ cd quentinha-app
$ npm i
$ react-native run-android
</code>
</pre>
## Firebase Example: 
### Imports:
<pre>
<code>
  import firebase from 'firebase';
  import '@firebase/firestore'
</code>
</pre>

### Methods:
<pre>
<code>
  //call function after the application initializes
  componentWillMount(){
  
    //firebase access data
    const config = {
      apiKey: "AIzaSyDyvGkpSeRXT5DbN8cl4JdcQdsG90I5GrI",
      authDomain: "quentinha-teste.firebaseapp.com",
      databaseURL: "https://quentinha-teste.firebaseio.com",
      projectId: "quentinha-teste",
      storageBucket: "quentinha-teste.appspot.com",
      messagingSenderId: "518985891734"
    };
    
    //init firebase
    firebase.initializeApp(config);
    
    //timestamp configuration for firestore
    firebase.firestore()
    .settings({
      timestampsInSnapshots:true
    });
    
    //entering data in firestore
    firebase.firestore()
    .collection("user")
    .doc()
    .set({
      name:"Paulo Henrique"
    });
  }
</code>
</pre>

## Contributing
Send us a Pull Request! Here is how:
1. Fork it!
2. Create your feature branch: git checkout -b my-new-feature
3. Stage your changes: git add .
3. Commit your changes: git commit -m 'Add some feature'
4. Push to the branch: git push origin my-new-feature
5. Submit a pull request

## License
<strong>The "quentinha" is licensed under the GNU general public license. See <a href="https://github.com/ColetivoEIDI/quentinha-app/blob/master/LICENSE">License</a> File for more information.</strong>
