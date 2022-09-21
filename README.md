<h1 align='center'>REACT NATIVE</h1>

<details>
<summary>All About React Native!</summary>

### `🤔 What is React-Native?`

> **React Native is a cross-platform mobile application development framework that Facebook created in 2015. React Native uses JavaScript as the underlying programming language, and it aims to help developers build native mobile apps for both Android and iOS devices with a single codebase.**

### `🤔 What Is Cross-Platform Development?`

> **Cross-platform development is the art of writing software that runs on different platforms; you write your codebase once and share it across different platforms. Cross-platform development provides you with a broad target audience since you have various options for running your codebase. For example, one app can be shared across both Android and iOS devices, resulting in a broader user base.**

### `🤔 What does meaning native apps?`

> **The term native app development refers to building a mobile app exclusively for a single platform. The app is built with programming languages and tools that are specific to a single platform. For example, you can develop a native Android app with Java or Kotlin and choose Swift and Objective-C for iOS apps.**

### `🤔 What is hybrid app?`

> **Hybrid apps combine both web applications created for web browser and native applications that are designed for a particular platform and have to be installed on a device.**

</details>

* ### ` For More About:`
* https://code.tutsplus.com/tutorials/what-is-react-native--cms-38028

### `🚨PREREQUISITES:`
* ***Html***
* ***Css***
* ***Javascript***
* ***React.js***

---

<h1 align='center'>Table Of Contents</h1>

### `💡Fundamentals:`

* [Setup React Native App](#setup)
* [View,Text]()
* [Styling Components]()
* [Apply Multiple Style]()
* [Buttons]()
* [Touchable]()
* [Pressable]()
* [List]()
* [FlatList]()
* [Section List]()
* [ScrollView]()
* [Refresh Control]()
* [Image & ImageBackground]()
* [Custom Fonts]()
* [Icons]()
* [Text Input]()
* [Switch]()
* [Checkbox]()
* [StausBar]()
* [Link]()
* [Alert & Toast Message]()
* [Modal]()
* [Async Storage]()
* `SQLite Database`
* [Activity Indicator]()
* [Web View]()
* [Copy Text]()
* [Splash Screen]()
* `Push Notification`
* `Google Maps`
* [Back Button Handler]()

### `💡Navigation:`
* [Stack Navigator]()
* [Tab Navigator]()
* [Material Bottom Tab Navigator]()
* [Material Top Navigator]()
* [Drawer Navigator]()
* [useNavigate Hook]()
* [Passing Data Between Screen]()
* [Header Styling]()

### 🚀 ***Generate Apk File:***
* `Create Account In Expo`
* `$ expo login`
* `$ expo build:android`
* **⌛ Wait 20-30 Minutes**

---

<h1 align='center'>Fundamentals</h1>

<a id='setup'></a>

### 📝Setup React Native App:
```bash
$ npm i expo
$ expo init my-app
```

<a id='setup'></a>

### 📝 View,Text:
```js
// View Like Html -> <div></div>
// Text Like Html -> <p></p>
import {View,Text} from 'react-native';

const Demo = () => {
   return(
      <View>
         <Text>Hello World</Text>
      </View>
   );
};

export default Demo;
```

<a id='setup'></a>

### 📝 Styling Components:
```js
import {
   View,Text,StyleSheet
} from 'react-native';
import {WebView} from 'react-native-webview';

const Demo = () => {
   return(
      <View style={styles.main}>
         <Text style={[styles.text,styles.white]}>Im A Text</Text>
      </View>
   );
};

const styles = StyleSheet.create({
   main:{
      margin: 20,
      backgroundColor: 'red',
      padding: 10,
      borderRadius: 5
   },
   text:{
      fontWeight: 'bold',
      textAlign: 'center',
   },
   // For Apple Multiple Style:
   white:{
      color: 'white'
   }
})

export default Demo;
```

### 📝 Button:
```js
import {Button} from 'react-native';

const Demo = () => {
   return(
      <Button
         title=''
         onPress={}
         color='red'
      >
         Open Link
      </Button>
   );
};

export default Demo;
```

### 📝 Touchable:
```js
import {
   View,Text,
   TouchableOpacity,
   TouchableHighlight,
   TouchableWithoutFeedback,
   Alert
} from 'react-native';

const Demo = () => {
   return(
      <View>
         <TouchableOpacity
            // onPress={}
            activeOpacity={0.7}
         >
            <View style={{backgroundColor:'red'}}>
               <Text style={{color: 'white',textAlign: 'center'}}>TouchableOpacity</Text>
            </View>
         </TouchableOpacity>
         <TouchableHighlight
            // onPress={}
            activeOpacity={0.7}
            underlayColor='#999'
         >
            <View style={{backgroundColor:'green'}}>
               <Text style={{color: 'white',textAlign: 'center'}}>TouchableHighlight</Text>
            </View>
         </TouchableHighlight>
         <TouchableWithoutFeedback
            // onPress={}
            onLongPress={()=>Alert.alert('ok')}
            activeOpacity={0.7}
            underlayColor='#999'
         >
            <View style={{backgroundColor:'orange'}}>
               <Text style={{color: 'white',textAlign: 'center'}}>TouchableWithoutFeedback</Text>
            </View>
         </TouchableWithoutFeedback>
      </View>
   );
};

export default Demo;
```

### 📝 Pressable:
```js
<Pressable 
   style={({pressed})=>({backgroundColor:pressed?'#999':'#999'})}
   disabled={false}
   android_ripple={{color:'yellow'}}
   onPress={()=>Alert.alert('onPress fired!')}
   onLongPress={()=>Alert.alert('onLongPress fired!')}
   delayLongPress={5000}
   hitSlop={{bottom:50}}
>
   <View>
      <Text style={styles.buttonText}>Click me</Text>
   </View>
</Pressable>
```

### 📝 FlatList:
```js
import {FlatList} from 'react-native';

const data = [
   {
      id: 1,
      name: 'Test
   }
]

const loadData = ({item}) => {
   return(
      <View>
         <Text>{item.name}</Text>
      <View>
   );
}

const Demo = () => {
   return(
      <View>
         <FlatList
            keyExtractor={(item) => item.id}
            data={data}
            renderItem={loadData}
            horizontal
            showHorizontalScrollIndicator={false}
            numColumns={2}
            inverted
         />
      </View>
   );
};

export default Demo;
```

### 📝 Section List:
```js
import {
   View,Text,SectionList
} from 'react-native';

const data = [
      {id:1,name:'Fruit1',data:['Apple','Orange']},
      {id:2,name:'Fruit2',data:['Apple','Orange']},
      {id:3,name:'Fruit3',data:['Apple','Orange']},
      {id:4,name:'Fruit4',data:['Apple','Orange']}
   ]

export default function Demo(){
   return(
     <View>
        <SectionList
            keyExtractor={(item,index)=>index}
            sections={data}
            renderSectionHeader={({section})=>{
               return <Text>{section.name}</Text>
            }}
            renderItem={({item})=>{
               return <Text>{item}</Text>
            }}
        />
     </View> 
   );
}
```

### 📝 ScrollView:
```js
import {ScrollView} from 'react-native';

const Demo = () => {
   return(
      <ScrollView>
         // write all things...
      </ScrollView>
   );
};

export default Demo;
```

### 📝 Refresh Control:
```js
import { useState } from 'react';
import {
   View,Text,FlatList,
   RefreshControl,ScrollView
} from 'react-native';

const myData = [
         {
            id: 1,
            name: 'Smith'
         },
         {
            id: 2,
            name: 'David'
         },
         {
            id: 3,
            name: 'John'
         },
         {
            id: 4,
            name: 'Doe'
         },
     ]

export default function Demo(){
   const [data,setData] = useState(myData)
   const [refreshing,setRefreshing] = useState(false)
   
   function RefreshHandler(){
      setRefreshing(true);
      let newData = [...data,{id:data.length+1,name:'rabbi'}]
      setData(newData);
      setRefreshing(false);
   }
   
   return(
      <View>
        <FlatList 
            keyExtractor={(item)=>item.id}
            data={data}
            renderItem={({item})=>{
               return(
                  <View>
                     <Text>{item.name}</Text>
                  </View>
               );
            }}
            refreshControl={
               <RefreshControl
                  refreshing={refreshing}
                  onRefresh={RefreshHandler}
                  colors={['red']}
               />
            }
        />
        <Text>{JSON.stringify(data)}</Text>
     </View>
   );
}
```

### 📝 Image & Image Background:
```js
import {Image} from 'react-native';

const Demo = () => {
   return(
      // Local Image:
      <Image source={require('../assets/demo.png')} />
      // For Remote Image:
      <Image source={{uri:'https://something.com/nature.png'}} />
   );
};

export default Demo;
```

### 📝 Custom Fonts:
* ***expo install @expo-google-fonts/baloo-bhai-2***
```js
// import {View,Text} from 'react-native';
import { useFonts,BalooBhai2_700Bold } from '@expo-google-fonts/baloo-bhai-2';

const Demo = () => {
   let [isFontLoaded] = useFonts({
      BalooBhai2_700Bold
   });
   
   if(!isFontLoaded){
      return null;
   }
   
   return(
      <View>
         <Text
            style={{fontFamily: 'BalooBhai2_700Bold'}}
         >
            Hello
         </Text>
      </View>
   );
};

export default Demo;
```
### 📝 Icons:
* ***expo install @expo/vector-icons***
```js
import {View,Text} from 'react-native';
import { FontAwesome5 } from '@expo/vector-icons';

const Demo = () => {
   return(
      <View>
         <Text
            style={{fontFamily: 'BalooBhai2_700Bold'}}
         >
            <FontAwesome5
               name='bars'
               size={26}
               color='red'
            />
         </Text>
      </View>
   );
};

export default Demo;
```

### 📝 Icons:
*  ***npm i @expo/vector-icons***
```js
import {
   View,Text
} from 'react-native';
import { FontAwesome5 } from '@expo/vector-icons';

export default function Demo(){
   return(
      <View>
        <FontAwesome5
            name='home'
            size={20}
            color='red'
        />
     </View>
   );
}
```

### 📝 Text Input:
```js
import {View,TextInput} from 'react-native';

const Demo = () => {
   return(
      <View>
         <TextInput
            // value='Hello'
            // onChangeText={}
            placeholder='Type your name...'
            // keyboardType='phone-pad' // --> phone-pad
            selectionColor='red'
            // maxLength={5}
            editable={true}
            // multiline
            secureTextEntry
         />
      </View>
   );
};

export default Demo;
```

### 📝 Switch:
```js
import {View,Switch} from 'react-native';

const Demo = () => {
   return(
      <View>
         <Switch
            value={true}
            // onValueChange={}
            tintColor='red'
            thumbColor='blue'
            trackColor='blue'
            // disabled
         />
      </View>
   );
};

export default Demo;
```

### 📝 Checkbox:
```js
import { useState } from 'react';
import {View,Text,Switch} from 'react-native';
import CheckBox from 'expo-checkbox';

const Demo = () => {
   const [checked,setChecked] = useState(false)
   
   function handleCheckbox(){
      setChecked(!checked);
   }
   
   return(
      <View style={{margin:10,flexDirection:'row'}}>
         <CheckBox
            value={checked}
            onValueChange={handleCheckbox}
            color={checked?'teal':'red'}
         />
         <Text 
            style={{marginLeft:5}}
         >I agree all tos.</Text>
      </View>
   );
};

export default Demo;
```

### 📝 StausBar:
```js
import {View,StatusBar} from 'react-native';

const Demo = () => {
   return(
      <View>
         <StatusBar
            backgroundColor='red'
            barStyle='light-content'
         />
      </View>
   );
};

export default Demo;
```

### 📝 Link:
```js
import {View,Link} from 'react-native';

const Demo = () => {
   return(
      <View>
         <Text onPress={Link.openURL('https://example.com')}>
            Click Me
         </Text>
      </View>
   );
};

export default Demo;
```

### 📝 Alert & Toast Message:
```js
import { useState } from 'react';
import {View,Text,Button,Alert,ToastAndroid} from 'react-native';
import CheckBox from 'expo-checkbox';

const Demo = () => {
   const [checked,setChecked] = useState(false)
   
   function handleAlert(){
      Alert.alert('Warning!','Are you sure you agree our terms of services...',[
            {text:'Ok',onPress:()=>console.log('Ok button pressed!')},
            {text:'Cancel',onPress:()=>console.log('Cancel button pressed!')},
            {text:'I know',onPress:()=>console.log('I know button pressed!')},
         ],{
            cancelable:true,
            onDismiss:()=>console.log('Back Button pressed!')
         });
   }
   
   function handleToast(){
      // ToastAndroid.show(
      //    'Hey there, im a toast message.',
      //    ToastAndroid.SHORT // --> SHORT/LONG
      // )
      
      // ToastAndroid.showWithGravity(
      //    'Hey there, im a toast message.',
      //    ToastAndroid.SHORT, // --> SHORT/LONG
      //    ToastAndroid.CENTER // --> TOP/BOTTOM/CENTER
      // )
      
      ToastAndroid.showWithGravityAndOffset(
         'Hey there, im a toast message.',
         ToastAndroid.SHORT, // --> SHORT/LONG
         ToastAndroid.TOP,0,0 // --> width & height
      )
   }
   
   return(
      <View style={{margin:10,flexDirection:'column'}}>
         <Button
            onPress={handleAlert}
            title='Alert'
            color='#784beb'
         />
         
         <Button
            onPress={handleToast}
            title='Toast'
            color='red'
         />
      </View>
   );
};

export default Demo;
```

### 📝 Modal:
```js
import { useState } from 'react';
import {
   View,Text,StyleSheet,
   Modal,Button
} from 'react-native';

const Demo = () => {
   const [isModalOpen,setIsModalOpen] = useState(false)
   
   function handleModal(){
      setIsModalOpen(!isModalOpen);
   }
   
   return(
      <View>
         <Modal
            visible={isModalOpen}
            onRequestClose={handleModal}
            transparent
            animationType='fade'
         >
            <View style={styles.modalContainer}>
               <View style={[styles.modal]}>
                  <Text style={styles.title}>Warning!</Text>
                  <Text style={styles.text}>Hey there, im a modal box.</Text>
                  <Button
                     onPress={handleModal}
                     title='I know'
                     color='teal'
                  />
               </View>
            </View>
         </Modal>
         <Button
            onPress={handleModal}
            title='Open Modal'
            color='green'
         />
      </View>
   );
};

const styles = StyleSheet.create({
   modalContainer:{
      flex: 1,
      justifyContent: 'center',
      alignItems: 'center'
   },
   modal:{
      backgroundColor: 'black',
      padding: 20,
      borderRadius: 5,
      height: 300,
      width: '90%'
   },
   title:{
      fontSize: 40,
      color: 'white'
   },
   text:{
      fontSize: 22,
      color: '#ededed'
   }
})

export default Demo;
```

### 📝 AsyncStorage:
```js
// It's like Javascript localStorage
import { AsyncStorage } from 'react-native';

AsyncStorage.setItem()
AsyncStorage.getItem()
AsyncStorage.removeItem()
AsyncStorage.mergeItem()
AsyncStorage.clear()
```

### 📝 SQLite Database:
```js

```

### 📝 Activity Indicator:
```js
// it's a spinner
import {ActivityIndicator} from 'react-native';

<ActivityIndicator
   color='red'
   size={60}
/>
```

### 📝 Web View:
* `$ npm i react-native-webview`
```js
import {
   StatusBar
} from 'expo-status-bar';
import React, {
   useState,
   useRef,
   useEffect
} from 'react';
import {
   Alert,
   Button,
   ActivityIndicator,
   Linking,
   SafeAreaView,
   StyleSheet,
   BackHandler,View,Text
} from 'react-native';
import {
   WebView
} from 'react-native-webview';

export default function Web() {
   const webViewRef = useRef()
   const [isLoadong,setLoading] = useState(false);

   // Error component:
   function Err(){
      return(
        <View style={{
          flex:1,
          height: 300,
          //width: '100%',
          backgroundColor: 'red'
        }}>
           <Text>Error</Text>
        </View> 
      );
   }
   
   // Go Back:
   function handleBackButtonPress(){
      try {
         webViewRef.current.goBack()
      } catch (err) {
         console.log("[handleBackButtonPress] Error : ", err.message)
      }
   }

   // Go Forword:
   function handleForwordButtonPress() {
      try {
         webViewRef.current.goForward()
      } catch (err) {
         console.log("[handleBackButtonPress] Error : ", err.message)
      }
   }
   
   // Stop Loading:
   function handleStopButtonPress() {
      try {
         webViewRef.current.stopLoading()
      } catch (err) {
         console.log("[handleBackButtonPress] Error : ", err.message)
      }
   }
   
   // Reload:
   function handleReloadButtonPress() {
      try {
         webViewRef.current.reload()
      } catch (err) {
         console.log("[handleBackButtonPress] Error : ", err.message)
      }
   }

   useEffect(() => {
      BackHandler.addEventListener("hardwareBackPress", handleBackButtonPress)
      return () => {
         BackHandler.removeEventListener("hardwareBackPress", handleBackButtonPress)
      };
   }, []);

   return (
      <SafeAreaView style={styles.safeArea}>
            <Button
         title='Go Back'
         color='purple'
         onPress={handleBackButtonPress}
         />
            <Button
         title='Go Forword'
         color='deeppink'
         onPress={handleForwordButtonPress}
         />
            <Button
         title='Stop Loading'
         color='#222'
         onPress={handleStopButtonPress}
         />
            <Button
         title='Reload'
         color='#6421db'
         onPress={handleReloadButtonPress}
         />
         <Err/>
            <WebView
         //  originWhiteList={['*']}
         source={ { uri: 'https://google.com' }}
         style={styles.container}
         ref={webViewRef}
         onError={()=> {
            // Alert.alert('Error!', 'Please check your internet connection')
            return <Err/>
         }}
         onLoadStart={(syntheticEvent) => {
            setLoading(true);
         }}
         //  onShouldStartLoadWithRequest={(event)=>{
         //     if (event.navigationType === 'click') {
         //          if (!event.url.match(/(google\.com\/*)/) ) {
         //              Linking.openURL(event.url)
         //              return false
         //          }
         //          return true
         //     }
         //     else{
         //          return true;
         //     }
         //  }}
         onLoadEnd={(syntheticEvent) => {
            setLoading(false);
         }}
         />
         {isLoadong && (
            <ActivityIndicator
               color="red"
               size="large"
               style={styles.loading}
            />
         )}
      </SafeAreaView>
   );
}

const styles = StyleSheet.create({
   safeArea: {
      flex: 1,
      backgroundColor: '#234356'
   },
   loading: {
      position: 'absolute',
      left: 0,
      right: 0,
      top: 0,
      bottom: 0,
      alignItems: 'center',
      justifyContent: 'center'
   },
   container: {
      flex: 1,
      backgroundColor: '#fff',
      alignItems: 'center',
      justifyContent: 'center',
   },
});
```

### 📝 Back Button Handler:
```js
useEffect(() => {
    const backAction = () => {
      Alert.alert("Hold on!", "Are you sure you want to go back?", [
       {
          text: "Cancel",
          onPress: () => null,
          style: "cancel"
       },
       { text: "YES", onPress: () => BackHandler.exitApp() }
      ]);
      handleBackButtonPress()
      // return true;
    };

    const backHandler = BackHandler.addEventListener(
      "hardwareBackPress",
      backAction
    );

    return () => backHandler.remove();
 }, []);
```

---

<h1 align='center'>Navigation</h1>

### 📝 Stack Navigator:
```js

```

### 📝 Tab Navigator:
```js

```

### 📝 Material Bottom Tab Navigator:
```js

```

### 📝 Material Top Tab Navigator:
```js

```

### 📝 Drawer Navigator:
* `npm i react-native-gesture-handler`
* `npm i react-native-reanimated`
* **babel.config.js**
```js
module.exports = function(api) {
  api.cache(true);
  return {
    presets: ['babel-preset-expo'],
    plugins: ['react-native-reanimated/plugin']
  };
};

```

### 📝 Passing Data Between Screen:
```js

```

### 📝 Header Styling:
```js

```