<h1 align='center'>REACT NATIVE</h1>

<details>
<summary>All About Of React Native!</summary>

### `🤔 What is React-Native?`

> **React Native is a cross-platform mobile application development framework that Facebook created in 2015. React Native uses JavaScript as the underlying programming language, and it aims to help developers build native mobile apps for both Android and iOS devices with a single codebase.**

### `🤔 What Is Cross-Platform Development?`

> **Cross-platform development is the art of writing software that runs on different platforms; you write your codebase once and share it across different platforms. Cross-platform development provides you with a broad target audience since you have various options for running your codebase. For example, one app can be shared across both Android and iOS devices, resulting in a broader user base.**

### `🤔 What does meaning native apps?`

> **The term native app development refers to building a mobile app exclusively for a single platform. The app is built with programming languages and tools that are specific to a single platform. For example, you can develop a native Android app with Java or Kotlin and choose Swift and Objective-C for iOS apps.**

### `🤔 What is hybrid app?`

> **Hybrid apps combine both web applications created for web browser and native applications that are designed for a particular platform and have to be installed on a device.**

</details>

* ### ***For More About:***
* https://code.tutsplus.com/tutorials/what-is-react-native--cms-38028

### `🚨PREREQUISITES:`
* ***Html***
* ***Css***
* ***Javascript***
* ***React.js***

### `🔥Learning Resources:`
1. ***Youtube:***
   * [Thapa Technical](https://youtube.com/playlist?list=PLwGdqUZWnOp354xMD8u0hxX-1qmCvfLiY)
   * [Programming With Mash](https://youtube.com/playlist?list=PL8kfZyp--gEXs4YsSLtB3KqDtdOFHMjWZ)
   * [Pradip Debnath](https://youtube.com/playlist?list=PLQWFhX-gwJblNXe9Fj0WomT0aWKqoDQ-h)

2. ***Websites:***
   * [JavatPoint](https://www.javatpoint.com/react-native-tutorial)
   * [Official Docs](https://reactnative.dev/docs/getting-started)
   * [React Navigation](https://reactnavigation.org/)

### `⚡Extra:`
* [Fonts Directory](https://directory.vercel.app/)
* [Icons](https://icons.expo.fyi/)
* [Expo](https://expo.dev/)

### `⏳How Many Does It Takes To Learn?`
 After learning HTML CSS JAVASCRIPT and REACT.Js it took me just ***9 days*** to learn all the following topics.

---

<h1 align='center'>Table Of Contents</h1>

<a id='Fundamentals'></a>

### `💡Fundamentals:`

* [Setup React Native App](#Setup)
* [View,Text](#View)
* [Styling Components](#Styling)
* [Buttons](#Button)
* [Touchable](#Touchable)
* [Pressable](#Pressable)
* `List` >> ***Like React.js***
* [FlatList](#FlatList)
* [Section List](#Section)
* [ScrollView](#ScrollView)
* [Refresh Control](#Refresh)
* [Image & ImageBackground](#Image)
* [Custom Fonts](#Fonts)
* [Icons](#Icons)
* [Text Input](#TextInput)
* [Switch](#Switch)
* [Checkbox](#Checkbox)
* [StausBar](#StausBar)
* [Link](#Link)
* [Alert & Toast Message](#Alert)
* [Modal](#Modal)
* [Async Storage](#AsyncStorage)
* `SQLite Database`
* [Activity Indicator](#ActivityIndicator)
* [Web View](#WebView)
* [Copy Text](#Copy)
* `Push Notification`
* `Google Maps`
* [Back Button Handler](#BackHandler)
* [Copy To Clipboard](#copyToClipboard)
* [Get NetInfo](https://github.com/react-native-netinfo/react-native-netinfo)
* [.env Variable](https://dev.to/dallington256/using-env-file-in-react-native-application-3961)
* `Fingerprint`

<a id='Navigation'></a>

### `💡Navigation:`
* [Native Stack Navigator](#Native)
* [Bottom Tab Navigator](#Bottom)
* [Material Bottom Tab Navigator](#MaterialBottom)
* [Material Top Tab Navigator](#MaterialTop)
* [Drawer Navigator](#Drawer)
* [useNavigate Hook](#useNavigate)
* [Passing Data Between Screen](#Passing)

### 🚀 ***Generate Apk File:***
* `Create Account In Expo`
* `$ expo login`
* `$ expo build:android`
* **⌛ Wait 20-30 Minutes**

---

<h1 align='center'>Fundamentals</h1>

<a id='Setup'></a>

### 📝Setup React Native App:
```bash
$ npm i expo
$ expo init my-app
```

<a id='setup'></a>
[**⬆ Back to Top**](#Fundamentals)

<a id='View'></a>

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
[**⬆ Back to Top**](#Fundamentals)

<a id='Styling'></a>

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
[**⬆ Back to Top**](#Fundamentals)

<a id='Button'></a>

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

<a id='setup'></a>
[**⬆ Back to Top**](#Fundamentals)

<a id='Touchable'></a>

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
[**⬆ Back to Top**](#Fundamentals)

<a id='Pressable'></a>

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
[**⬆ Back to Top**](#Fundamentals)

<a id='FlatList'></a>

### 📝 FlatList:
```js
import {FlatList} from 'react-native';

const data = [
   {
      id: 1,
      name: 'Test'
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
[**⬆ Back to Top**](#Fundamentals)

<a id='Section'></a>

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

<a id='setup'></a>

[**⬆ Back to Top**](#Fundamentals)

<a id='ScrollView'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='Refresh'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='Image'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='Fonts'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='Icons'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='TextInput'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='Switch'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='Checkbox'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='StausBar'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='Link'></a>

### 📝 Link:
```js
import {View,Linking} from 'react-native';

const Demo = () => {
   return(
      <View>
         <Text onPress={Linking.openURL('https://example.com')}>
            Click Me
         </Text>
      </View>
   );
};

export default Demo;
```

[**⬆ Back to Top**](#Fundamentals)

<a id='Alert'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='Modal'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='AsyncStorage'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='SQLite'></a>

### 📝 SQLite Database:
```js

```

[**⬆ Back to Top**](#Fundamentals)

<a id='ActivityIndicator'></a>

### 📝 Activity Indicator:
```js
// it's a spinner
import {ActivityIndicator} from 'react-native';

<ActivityIndicator
   color='red'
   size={60}
/>
```

[**⬆ Back to Top**](#Fundamentals)

<a id='WebView'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='Copy'></a>

### 📝 Copy Text:
```js
<Text selectable={true}></Text>
```

[**⬆ Back to Top**](#Fundamentals)

<a id='BackHandler'></a>

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

[**⬆ Back to Top**](#Fundamentals)

<a id='copyToClipboard'></a>

### 📝 Copy To Clipboard:
* ***expo install expo-clipboard***
```
import * as Clipboard from 'expo-clipboard';

// For copy:
const copyToClipboard = async (link) => {
   await Clipboard.setStringAsync(link);
      ToastAndroid.show(
         'Copied successfuly!',
         ToastAndroid.SHORT
      )
};
   
// For Get Copied Text:
const getClipboardText = async (link) => {
   let text = await Clipboard.getStringAsync();
};

```

[**⬆ Back to Top**](#Fundamentals)

---

<h1 align='center'>Navigation</h1>

<a id='Native'></a>

### 📝 Native Stack Navigator:

<details>
<summary>View Code...</summary>

* ***App.js***
```js
import React, { useState,useEffect } from 'react';
import {
   View,Text,StyleSheet,
   FlatList,Alert,
   TouchableOpacity,
   Button,ScrollView,StatusBar,
   TextInput,Image,ImageBackground
} from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { createNativeStackNavigator } from '@react-navigation/native-stack';

const Demo = () => {
   const Stack = createNativeStackNavigator()
   
   return(
     <NavigationContainer>
         <StatusBar/>
         <Stack.Navigator
            initialRouteName='Home'
            screenOptions={{
               headerStyle:{
                  // backgroundColor:'#222',
               },
               headerTitleStyle:{
                  color:'white'
               },
               headerTintColor:'white',
               headerTitleAlign:'center',
               headerShown:true,
               // headerShadowVisible:true,
               // headerTransparent:true,
               headerBackground:()=>{
                  return(<ImageBackground
                     source={require('./assets/header.jpg')}
                  />)
               },
               headerTintColor:'red',
               headerBackVisible:false,
               headerLeft:()=>{
                  return(
                     <Text style={{color:'white'}}>⬅️ Go Back</Text>
                  )
               },
               headerRight:()=>{
                  return(
                     <Text style={{color:'white'}}>🏠 Go Home</Text>
                  )
               },
               // headerTitle:''
               header:({navigation,route,options})=>{
                  return(
                     <View style={{backgroundColor:'#807beb',padding:10}}>
                        <Text>Hello Im Custom Header</Text>
                        
                     </View>
                  )
               },
               statusBarAnimation:'slide',
               statusBarColor:'cyan',
               animation:'slide_from_bottom',
               presentation:'fullScreenModal',
               orientation:'all',
               navigationBarColor:'teal',
               navigationBarHidden:false,
               
            }}
         >
            <Stack.Screen
               name='Home'
               component={Home}
            />
            <Stack.Screen
               name='About'
               component={About}
            />
            <Stack.Screen
               name='Contact'
               component={Contact}
            />
            <Stack.Screen
               name='Profile'
               component={Profile}
            />
         </Stack.Navigator>
     </NavigationContainer>
   );
};

const styles = StyleSheet.create({
   container:{
      
   }
})

export default Demo;


// Screen:
function Home({navigation}){
   return(
     <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
        <Text style={{fontWeight:'bold'}}>Home Screen</Text>
        <View>
           <Button
            color='#784beb'
            title='About'
            onPress={()=>navigation.navigate('About')}
           />
           <Button
            color='#333'
            title='Contact'
            onPress={()=>navigation.navigate('Contact')}
           />
           <Button
            color='green'
            title='Profile'
            onPress={()=>navigation.navigate('Profile',{id:100,name:'Adams Smith'})}
           />
        </View>
     </View> 
   );
}

function About({navigation}){
   return(
     <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
        <Text style={{fontWeight:'bold'}}>About Screen</Text>
        <Button
         color='#50aee3'
         title='Go Contact'
         onPress={()=>navigation.navigate('Contact')}
        />
     </View> 
   );
}

function Contact({navigation}){
   return(
     <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
        <Text style={{fontWeight:'bold'}}>Contact Screen</Text>
        <Button
         color='#50aee3'
         title='Go Home'
         onPress={()=>navigation.navigate('Home')}
        />
     </View> 
   );
}

function Profile({navigation,route}){
   return(
     <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
        <Text style={{fontWeight:'bold'}}>Profile Screen</Text>
        <Button
            color='#f7407b'
            title='Go Back'
            onPress={()=>navigation.goBack()}
        />
        <Text>{JSON.stringify(route.params)}</Text>
        <Text style={{fontSize:30,fontWeight:'bold'}}>Hey, {route.params.name}</Text>
     </View> 
   );
}
```

</details>

[**⬆ Back to Top**](#Navigation)

<a id='Bottom'></a>

### 📝 Bottom Tab Navigator:

<details>
<summary>View Code...</summary>

* ***App.js***
```js
import React, { useState,useEffect } from 'react';
import {
   View,Text,StyleSheet,
   FlatList,Alert,
   TouchableOpacity,
   Button,ScrollView,StatusBar,
   TextInput,Image,ImageBackground
} from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { createBottomTabNavigator } from '@react-navigation/bottom-tabs';
import { FontAwesome5 } from '@expo/vector-icons';

const Demo = ({route}) => {
   const Tab = createBottomTabNavigator()
   
   return(
     <NavigationContainer>
         <StatusBar/>
         <Tab.Navigator
            initialRouteName='Home'
            screenOptions={{
               backBehavior:'history',
               // title:'Hello'
               tabBarShowLabel:true,
               tabBarLabelStyle:{
                  fontWeight:'bold'
               },
               // tabBarBadge:3,
               // tabBarButton: (props) => <TouchableOpacity {...props} />,
               tabBarActiveTintColor:'white',
               tabBarInactiveTintColor:'#555',
               tabBarActiveBackgroundColor:'#8c4deb',
               tabBarInactiveBackgroundColor:'#ededed',
               tabBarHideOnKeyboard:true,
               tabBarStyle:{
                  height:100,
                  backgroundColor:'#999',
                  // padding:10,
                  // marginBottom:10
               },
               // tabBarBackground: () => (
               //    <Image
               //       source={require('./assets/header.jpg')}
               //    />
               // ),
               // headerStyle:{
               //    height:70,
               //    backgroundColor:'yellow',
               // },
               headerShown:true,
               header:({navigation,route,options,layout})=>{
                  return(
                     <View>
                        <Text></Text>
                        <View style={{backgroundColor:'cyan',height:100}}>
                           <Text style={{color:'black',margin:2}}>{route.name}</Text>
                           <Text style={{color:'black',margin:2}}>{JSON.stringify(route)}</Text>
                        </View>
                     </View>
                  )
               }
            }}
            

         >
            <Tab.Screen
               name='Home'
               component={Home}
               options={{
                  tabBarIcon:({focused,size,color})=>{
                     return(
                        <FontAwesome5
                           name='home'
                           size={focused?27:22}
                           color={color}
                        />
                     )
                  }
               }}
            />
            <Tab.Screen
               name='About'
               component={About}
               options={{
                  tabBarIcon:({focused,size,color})=>{
                     return(
                        <FontAwesome5
                           name='envelope'
                           size={focused?27:22}
                           color={color}
                        />
                     )
                  }
               }}
            />
            <Tab.Screen
               name='Contact'
               component={Contact}
               options={{
                  tabBarIcon:({focused,size,color})=>{
                     return(
                        <FontAwesome5
                           name='info'
                           size={focused?27:22}
                           color={color}
                        />
                     )
                  }
               }}
            />
            <Tab.Screen
               name='Profile'
               component={Profile}
               options={{
                  tabBarIcon:({focused,size,color})=>{
                     return(
                        <FontAwesome5
                           name='user'
                           size={focused?27:22}
                           color={color}
                        />
                     )
                  }
               }}
            />
         </Tab.Navigator>
     </NavigationContainer>
   );
};

const styles = StyleSheet.create({
   container:{
      
   }
})

export default Demo;


// Screen:
function Home({navigation}){
   return(
     <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
        <Text style={{fontWeight:'bold'}}>Home Screen</Text>
        <View>
           <Button
            color='#784beb'
            title='About'
            onPress={()=>navigation.navigate('About')}
           />
           <Button
            color='#333'
            title='Contact'
            onPress={()=>navigation.navigate('Contact')}
           />
           <Button
            color='green'
            title='Profile'
            onPress={()=>navigation.navigate('Profile',{id:100,name:'Adams Smith'})}
           />
        </View>
     </View> 
   );
}

function About({navigation}){
   return(
     <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
        <Text style={{fontWeight:'bold'}}>About Screen</Text>
        <Button
         color='#50aee3'
         title='Go Contact'
         onPress={()=>navigation.navigate('Contact')}
        />
     </View> 
   );
}

function Contact({navigation}){
   return(
     <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
        <Text style={{fontWeight:'bold'}}>Contact Screen</Text>
        <Button
         color='#50aee3'
         title='Go Home'
         onPress={()=>navigation.navigate('Home')}
        />
     </View> 
   );
}

function Profile({navigation,route}){
   return(
     <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
        <Text style={{fontWeight:'bold'}}>Profile Screen</Text>
        <Button
            color='#f7407b'
            title='Go Back'
            onPress={()=>navigation.goBack()}
        />
        <Text>{JSON.stringify(route.params)}</Text>
        <Text style={{fontSize:30,fontWeight:'bold'}}>Hey,</Text>
     </View> 
   );
}
```

</details>

[**⬆ Back to Top**](#Navigation)

<a id='MaterialBottom'></a>

### 📝 Material Bottom Tab Navigator:

<details>
<summary>View Code...</summary>

* ***App.js***
```js
import React, { useState,useEffect } from 'react';
import {
   View,Text,StyleSheet,
   FlatList,Alert,
   TouchableOpacity,
   Button,ScrollView,StatusBar,
   TextInput,Image
} from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { createNativeStackNavigator } from '@react-navigation/native-stack';
import { createBottomTabNavigator } from '@react-navigation/bottom-tabs';
import { createMaterialBottomTabNavigator } from '@react-navigation/material-bottom-tabs';
import { FontAwesome5 } from '@expo/vector-icons';

const Demo = () => {
   const Stack = createNativeStackNavigator();
   const Tab = createMaterialBottomTabNavigator();
   
   return(
    <NavigationContainer>
       <Tab.Navigator 
         initialRouteName='Home'
         screenOptions={{
            shifting:true,
            tabBarColor:'red'
         }}
         activeColor='white'
         inactiveColor='#ededed'
         barStyle={{backgroundColor:'teal',paddingBottom: 10}}
         
       >
         <Tab.Screen 
            name="Home" 
            component={Home} 
            options={{
               // title:''
               tabBarIcon:({color})=>{
                  return(
                     <FontAwesome5
                        name='home'
                        color={color}
                        size={20}
                     />
                  )
               }
            }}   
         />
         <Tab.Screen name="User" component={User} />
         <Tab.Screen name="Contact" component={Contact} />
       </Tab.Navigator>
    </NavigationContainer>
   );
};

const styles = StyleSheet.create({
   container:{
      
   }
})

export default Demo;

// Screens:
function Home({navigation}){
   return(
      <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
         <Text style={{fontWeight:'bold'}}>Home Screen</Text>
         <Button
            color='red'
            title='Contact'
            onPress={()=>navigation.navigate('User')}
         />
      </View>  
   )
}

function User(){
   return(
      <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
         <Text style={{fontWeight:'bold'}}>User Screen</Text>
      </View>  
   )
}

function Contact(){
   return(
      <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
         <Text style={{fontWeight:'bold'}}>Contact Screen</Text>
      </View>  
   )
}


```

</details>

[**⬆ Back to Top**](#Navigation)

<a id='MaterialTop'></a>

### 📝 Material Top Tab Navigator:
<details>
<summary>View Code...</summary>

* ***App.js***
```js
import React, { useState,useEffect } from 'react';
import {
   View,Text,StyleSheet,
   FlatList,Alert,
   TouchableOpacity,
   Button,ScrollView,StatusBar,
   TextInput,Image
} from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { createNativeStackNavigator } from '@react-navigation/native-stack';
import { createBottomTabNavigator } from '@react-navigation/bottom-tabs';
import { createMaterialTopTabNavigator } from '@react-navigation/material-top-tabs';
import { FontAwesome5 } from '@expo/vector-icons';

const Demo = () => {
   const Stack = createNativeStackNavigator();
   const Tab = createMaterialTopTabNavigator();
   
   return(
    <NavigationContainer>
       <StatusBar/>
       <Tab.Navigator 
         initialRouteName='Home'
         screenOptions={{
            tabBarLabelStyle:{fontSize:15},
            tabBarShowIcon:false,
            tabBarPressColor:'#ededed',
            tabBarActiveTintColor:'#4598e7',
            tabBarInactiveTintColor:'#999'
         }}
         activeColor='white'
         inactiveColor='#ededed'
         barStyle={{backgroundColor:'teal',paddingBottom: 10}}
         tabBarPosition='top'
         backBehavior='order'
       >
         <Tab.Screen 
            name="Home" 
            component={Home} 
            options={{
               // title:''
               tabBarIcon:({color})=>{
                  return(
                     <FontAwesome5
                        name='home'
                        color={color}
                        size={20}
                     />
                  )
               }
            }}   
         />
         <Tab.Screen name="User" component={User} />
         <Tab.Screen name="Contact" component={Contact} />
       </Tab.Navigator>
    </NavigationContainer>
   );
};

const styles = StyleSheet.create({
   container:{
      
   }
})

export default Demo;

// Screens:
function Home({navigation}){
   return(
      <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
         <Text style={{fontWeight:'bold'}}>Home Screen</Text>
         <Button
            color='red'
            title='Contact'
            onPress={()=>navigation.navigate('User')}
         />
      </View>  
   )
}

function User(){
   return(
      <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
         <Text style={{fontWeight:'bold'}}>User Screen</Text>
      </View>  
   )
}

function Contact(){
   return(
      <View style={{flex:1,justifyContent:'center',alignItems:'center'}}>
         <Text style={{fontWeight:'bold'}}>Contact Screen</Text>
      </View>  
   )
}


```

</details>

[**⬆ Back to Top**](#Navigation)

<a id='Drawer'></a>

### 📝 Drawer Navigator:
* `npm i react-native-gesture-handler`
* `npm i react-native-reanimated`
* ***babel.config.js:***
```js
module.exports = function(api) {
  api.cache(true);
  return {
    presets: ['babel-preset-expo'],
    plugins: ['react-native-reanimated/plugin']
  };
};
```

<details>
<summary>View Code...</summary>

* ### `Default Drawer Navigator:`
* ***App.js***
```js
import 'react-native-gesture-handler';
import * as React from 'react';
import { Button, View, Text, StatusBar } from 'react-native';
import { createDrawerNavigator } from '@react-navigation/drawer';
import { NavigationContainer } from '@react-navigation/native';
import Demo from './component/Demo'
import MyWeb from './component/Web'
import Back from './component/Back'
import {useFonts,BalooBhai2_500Medium} from '@expo-google-fonts/baloo-bhai-2';
import { FontAwesome5 } from '@expo/vector-icons';

const Drawer = createDrawerNavigator();

function Home(){
   return(
     <Text>Hello</Text> 
   );
}


export default function App() {
  
  let [fontsLoad] = useFonts({
     BalooBhai2_500Medium
  });
  
  if(!fontsLoad){
     return null;
  }
  
  return (
    <NavigationContainer>
      <StatusBar 
         backgroundColor='#333'
         barStyle='light-content'
      />
      <Drawer.Navigator 
         useLegacyImplementation={true} 
         initialRouteName="Home"
         screenOptions={{
            drawerPosition:'left',
            drawerType:'slide',
            swipeEdgeWidth:500,
            drawerHideStatusBarOnOpen:false,
            overlayColor:'#00000055',
            drawerStyle:{backgroundColor:'#ededed',width:250},
            headerShown:true,
            headerTitleAlign:'center',
            headerStyle:{backgroundColor:'#333'},
            headerTintColor:'white',
            headerTitleStyle:{fontSize:30,fontFamily:'BalooBhai2_500Medium'},
            
            swipeEnabled:true,
            gestureEnabled:true,
            
            drawerActiveBackgroundColor:'deeppink',
            drawerActiveTintColor:'white',
            drawerItemStyle:{fontWeight:'bold'},
            drawerLabelStyle:{fontWeight:'bold',marginLeft:-25},
            
            
         }}
      >
        <Drawer.Screen 
            name="Home" 
            component={Home}
            options={{
               title:'Home',
               drawerIcon:({focused,color,size})=>{
                  return(
                  <FontAwesome5
                     name='home'
                     size={20}
                     color={focused?'white':'#333'}
                  />
                  )
               }
            }}
         />
        <Drawer.Screen 
            name="Demo" 
            component={Demo} 
            options={{
               title:'User',
               drawerIcon:({focused,color,size})=>{
                  return(
                  <FontAwesome5
                     name='user'
                     size={20}
                     color={focused?'white':'#333'}
                  />
                  )
               }
            }}
        />
        <Drawer.Screen 
            name="MyWeb" 
            component={MyWeb} 
            options={{
               title: 'Email',
               drawerIcon:({focused,color,size})=>{
                  return(
                  <FontAwesome5
                     name='envelope'
                     size={20}
                     color={focused?'white':'#333'}
                  />
                  )
               }
            }}   
         />
        <Drawer.Screen 
            name="Back" 
            component={Back} 
            options={{
               drawerIcon:({focused,color,size})=>{
                  return(
                  <FontAwesome5
                     name='btc'
                     size={20}
                     color={focused?'white':'#333'}
                  />
                  )
               }
            }}   
         />
      </Drawer.Navigator>
    </NavigationContainer>
  );
}
```

* ### `Custom Drawer Navigator:`
* ***App.js***
```js
import 'react-native-gesture-handler';
import React, { useState,useEffect } from 'react';
import {
   View,Text,StyleSheet,
   FlatList,Alert,
   TouchableOpacity,
   Button,ScrollView,StatusBar,
   TextInput,Image
} from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { createNativeStackNavigator } from '@react-navigation/native-stack';
import { createDrawerNavigator } from '@react-navigation/drawer';
import Demo from './component/Demo'
import MyWeb from './component/Web'
import Back from './component/Back'
import CustomDrawer from './CustomDrawer.js';
import { FontAwesome5 } from '@expo/vector-icons';

const App = () => {
   const Drawer = createDrawerNavigator()
   
   return(
    <NavigationContainer>
       <Drawer.Navigator 
         initialRouteName='Back'
         drawerContent={props => <CustomDrawer {...props}/>}
         screenOptions={{
            drawerPosition:'left',
            drawerActiveBackgroundColor:'#5935db',
            drawerActiveTintColor:'white',
            drawerLabelStyle:{marginLeft:-25}
         }}
      >
         <Drawer.Screen 
            name="Demo" 
            component={Demo} 
            options={{
               drawerIcon:({name,size,color})=>{
                  return <FontAwesome5 name='home' size={25} color={color} />
               }
            }}
         />
         <Drawer.Screen 
            name="MyWeb" 
            component={MyWeb}
            options={{
               drawerIcon:({name,size,color})=>{
                  return <FontAwesome5 name='envelope' size={25} color={color} />
               }
            }}
         />
         <Drawer.Screen 
            name="Back" 
            component={Back} 
            options={{
               drawerIcon:({name,size,color})=>{
                  return <FontAwesome5 name='user' size={25} color={color} />
               }
            }}   
         />
       </Drawer.Navigator>
    </NavigationContainer>
   );
};

const styles = StyleSheet.create({
   container:{
      
   }
})

export default App;
```

* ***CustomDrawer.js***
```js
import React, { useState,useEffect } from 'react';
import {
   View,Text,StyleSheet,
   FlatList,Alert,
   TouchableOpacity,
   Button,ScrollView,StatusBar,
   TextInput,Image,ImageBackground
} from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { DrawerContentScrollView,DrawerItemList } from '@react-navigation/drawer';

const CustomDrawer = (props) => {
   return(
     <DrawerContentScrollView {...props}>
         <View style={{backgroundColor:'#2821d9',height:200,marginBottom:20}}>
            <ImageBackground
               style={{width:'100%',height:undefined}}
               source={require('./assets/header.jpg')}
            >
               <Image 
                  source={require('./assets/user.jpg')}
                  style={{height:50,width:50,marginLeft:10,marginTop:20}}
                  resizeMode='cover'
               />
               <Text style={{color:'white',marginLeft:10,marginTop:10}}>You Have $20 Remaining</Text>
            </ImageBackground>
         </View>
         <View>
            <DrawerItemList {...props}/>
         </View>
         <View style={{marginTop:800}}>
            <Text>Hello</Text>
         </View>
     </DrawerContentScrollView>
   );
};

const styles = StyleSheet.create({
   container:{
      
   }
})

export default CustomDrawer;
```

</details>

[**⬆ Back to Top**](#Navigation)

<a id='useNavigate'></a>

### 📝 useNavigate Hook:
```js
import {useNavigate} from 'react-native;
const navigation = useNavigate();

// Usage:
navigation.navigate('Screen_Name');
```

[**⬆ Back to Top**](#Navigation)

<a id='Passing'></a>

### 📝 Passing Data Between Screen:
```js
navigation.navigate('User',{id:100,name:'Smith'})
```

[**⬆ Back to Top**](#Navigation)
