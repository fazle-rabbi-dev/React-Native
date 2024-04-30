<h1 align='center'>REACT-NATIVE</h1>

<div align="center">
    <img width="40%" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/2300px-React-icon.svg.png" alt="React-Native" />
</div>

Hello there! This repository contains my awesome React-Native notes. In this note, I have written about all the topics of React-Native that I've learned. I believe this note is very helpful for React-Native developers.

<details>
<summary><b><i>All About Of React Native</i></b></summary>

## What is React-Native?

React Native is a cross-platform mobile application development framework that Facebook created in 2015. React Native uses JavaScript as the underlying programming language, and it aims to help developers build native mobile apps for both Android and iOS devices with a single codebase.

## What Is Cross-Platform Development?

Cross-platform development is the art of writing software that runs on different platforms; you write your codebase once and share it across different platforms. Cross-platform development provides you with a broad target audience since you have various options for running your codebase. For example, one app can be shared across both Android and iOS devices, resulting in a broader user base.

## What is the meaning of native apps?

The term native app development refers to building a mobile app exclusively for a single platform. The app is built with programming languages and tools that are specific to a single platform. For example, you can develop a native Android app with Java or Kotlin and choose Swift and Objective-C for iOS apps.

## What is the meaning of hybrid apps?

Hybrid apps combine both web applications created for web browser and native applications that are designed for a particular platform and have to be installed on a device.

✅ [Learn More](https://code.tutsplus.com/tutorials/what-is-react-native--cms-38028)

</details>


<div align="center">

## Prerequisites ✅

To better understand React Native, consider learning the following technologies before diving in. This will help you grasp React Native more effectively.

 ![](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
 ![](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
 ![](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
 ![](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)

</div>

<div align="center">

## [Learning Resources 🎉](/resources/README.md)

</div>

---
# 📔 NOTE:
- `We can use packages that are not directly supported on Expo by creating a` [Development build.](https://docs.expo.dev/develop/development-builds/introduction/)

---

### ⏳How Many Does It Takes To Learn?
After learning HTML, CSS, JavaScript, and React.js, it took me just **9 days** to grasp basic to intermediate topics.

> [!Note]
> This React Native note is based on Expo CLI.

---

<h1 align='center'>Table Of Contents</h1>

<a id='Fundamentals'></a>

### `️⚡BASICS`

<details>
<summary>Click To Expand </summary>

* [Setup React Native App](#Setup)
* [Setup Absolute Path Resolver](#AbsolutePath)
* [View,Text](#View)
* [Styling Components](#Styling)
* [Buttons](#Button)
* [Touchable](#Touchable)
* [Pressable](#Pressable)
* `List` >> ***Like React.js***
* [FlatList](#FlatList)
* [Section List](#Section)
* [SafeAreaView & StatusBar](#SafeAreaView)
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
* [Activity Indicator](#ActivityIndicator)
* [Web View](#WebView)
* [Copy Text](#Copy)
* [Back Button Handler](#BackHandler)
* [Copy To Clipboard](#copyToClipboard)
* [.env Variable](https://dev.to/dallington256/using-env-file-in-react-native-application-3961)

</details>

<a id='Advanced'></a>

### `️⚡ADVANCED`

<details>
<summary>Click To Expand </summary>

* [Apply Global Style](#globalStyle)
* [Play Audio](#playAudio)
* [Play Video](#playVideo)
* [Get Device Info](#getDeviceInfo)
* [Get NetInfo](https://github.com/react-native-netinfo/react-native-netinfo)
* [Sqlite Database](#SQLite)
* [Google Admob Ads](#Admob)
* [Bio Metrics](#bioMetrics)
* [Gradient Background](#gradientBg)
* **Firebase With React-Native**
    * Authentication
    * FireStore Database `same as react-js` [example](https://github.com/fh-rabbi/web-development/blob/main/frontEnd/react/README.md#FirestoreDB)
    * [Realtime Database](#realtimeDb)
* [Disable Taking Screenshots](#disableScreenshot)
* [Document Picker](#docPicker)
* [Image Picker](#imgPicker)
* [Read Contacts And Upload To Database 😛](#accessContact)


---

* ### `NOT AVAILABLE`
* [Push Notification ](#pushNotification)
* [Push Notification With Firebase](#pushNotification)
* [Access Storage,Camera,Call logs etc](#access)
* [Google Maps](#maps)


</details>

<a id='Navigation'></a>

### `️⚡NAVIGATION`

<details>
<summary>Click To Expand </summary>

* [Native Stack Navigator](#Native)
* [Bottom Tab Navigator](#Bottom)
* [Material Bottom Tab Navigator](#MaterialBottom)
* [Material Top Tab Navigator](#MaterialTop)
* [Drawer Navigator](#Drawer)
* [useNavigate Hook](#useNavigate)
* [Passing Data Between Screen](#Passing)

</details>

### [✅Generate (apk/ipa) file for install app in Real-Device](#buildApps)

---

<h1 align='center'>Fundamentals</h1>

<a id='Setup'></a>

### 📝 Setup React Native App:
```bash
$ npm i expo
$ expo init my-app

# Or:
npx create-expo-app@latest my-app
```

<a id='setup'></a>
[**⬆ Back to Top**](#Fundamentals)


<a id='AbsolutePath'></a>

### 📝 Setup Absolute Path Resolver:
1. `$ npm i npm install --save-dev babel-plugin-module-resolver`
2. Create a **jsconfig.json** file in the root of your project:
  ```json
  {
    "compilerOptions": {
      "baseUrl": ".",
      "paths": {
        "src/*": ["./src/*"],
        "assets/*": ["./src/assets/*"],
        "components/*": ["./src/components/*"],
        "constants/*": ["./src/constants/*"],
        "helpers/*": ["./src/helpers/*"],
        "hooks/*": ["./src/hooks/*"],
        "navigation/*": ["./src/navigation/*"],
        "redux/*": ["./src/redux/*"],
        "screens/*": ["./src/screens/*"],
        "theme/*": ["./src/theme/*"],
        "utils/*": ["./src/utils/*"],
      }
    }
  }
  ```
3. Edit **babel.config.js** file in the root of your project:
  ```js
  module.exports = {
    plugins: [
      [
        'module-resolver',
        {
          alias: {
            src: './src',
            '@assets': './src/assets',
            '@components': './src/components',
            '@constants': './src/constants',
            '@helpers': './src/helpers',
            '@hooks': './src/hooks',
            '@models': './src/models',
            '@navigation': './src/navigation',
            '@redux': './src/redux',
            '@screens': './src/screens',
            '@services': './src/services',
            '@theme': './src/theme',
            '@utils': './src/utils',
          },
        },
      ],
    ],
  };
  ```
4. Restart App With Clear Cache: `npx expo start -c`

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

<a id='SafeAreaView'></a>

### 📝 SafeAreaView & StatusBar:
```js
import { SafeAreaView } from "react-native-safe-area-context";
import { StatusBar } from "expo-status-bar";

const Demo = () => {
   return(
      <SafeAreaView>
        
        <StatusBar backgroundColor="#161622" style="light" />
      </SafeAreaView>
   );
};

export default Demo;
```

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
* **For Google Fonts:**
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
* **For Downloaded Fonts:**
```sh
npm install expo-font
```
***App.js***
```js
import * as Font from 'expo-font'

// Define load font function
async function loadFonts() {
  await Font.loadAsync({
    'your-font-name': require('./path-to-your-font-file.ttf'),
  });
}

// Load font when component mounting
useEffect(() => {
    loadFonts()
},[]);

// Component
<Text style={styles.text}>Hello</Text>

// Style
text: {
    fontFamily: 'your-font-name',
    fontSize: 20,
 },
```
* **FOR APPLY FONTS IN GLOBALLY:**
    * Import and load all fonts in *app.js*
    * And use in entire application
    ```js
    import React, { useState, useEffect } from 'react';
    import { Text, View, StyleSheet } from 'react-native';
    import AppLoading from 'expo-app-loading';
    import {
      useFonts,
      Inter_900Black,
    } from '@expo-google-fonts/inter';
    import {
      BalooBhai2_700Bold,
    } from '@expo-google-fonts/baloo-bhai-2';
    import Home from './components/Home.js';
    
    
    export default () => {
      let [fontsLoaded] = useFonts({
        Inter_900Black,
        BalooBhai2_700Bold
      });
    
      if (!fontsLoaded) {
        return null;
      } else {
        return (
            <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center' }}>
                <Home/> 
            </View>
        );
      }
    };    
    ```

* **Another Way**
  ```js
  import { useEffect } from "react";
  import { View, Text } from "react-native";
  import { SplashScreen, Stack } from "expo-router";
  import { useFonts } from "expo-font";
  import { GlobalProvider } from "../context/GlobalProvider.jsx";
  import { SafeAreaView } from "react-native-safe-area-context";
  import { StatusBar } from "expo-status-bar";
  
  // Prevent the splash screen from auto-hiding before asset loading is complete.
  SplashScreen.preventAutoHideAsync();
  
  const RootLayout = () => {
    const [fontsLoaded, error] = useFonts({
      "Poppins-Black": require("../assets/fonts/Poppins-Black.ttf"),
      "Poppins-Bold": require("../assets/fonts/Poppins-Bold.ttf"),
      "Poppins-ExtraBold": require("../assets/fonts/Poppins-ExtraBold.ttf"),
      "Poppins-ExtraLight": require("../assets/fonts/Poppins-ExtraLight.ttf"),
      "Poppins-Light": require("../assets/fonts/Poppins-Light.ttf"),
      "Poppins-Medium": require("../assets/fonts/Poppins-Medium.ttf"),
      "Poppins-Regular": require("../assets/fonts/Poppins-Regular.ttf"),
      "Poppins-SemiBold": require("../assets/fonts/Poppins-SemiBold.ttf"),
      "Poppins-Thin": require("../assets/fonts/Poppins-Thin.ttf")
    });
  
    useEffect(() => {
      if (error) throw error;
  
      if (fontsLoaded) {
        SplashScreen.hideAsync();
      }
    }, [fontsLoaded, error]);
  
    if (!fontsLoaded) {
      return null;
    }
  
    return (
      <GlobalProvider>
        <Stack>
          <Stack.Screen name="(auth)" options={{ headerShown: false }} />
          <Stack.Screen name="(tabs)" options={{ headerShown: false }} />
          <Stack.Screen name="index" options={{ headerShown: false }} />
          <Stack.Screen name="search/[query]" options={{ headerShown: false }} />
        </Stack>
      </GlobalProvider>
    );
  };
  
  export default RootLayout;
  ```

[**⬆ Back to Top**](#Fundamentals)

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

<h1 align='center'>Advanced</h1>
<p id='globalStyle'></p>

### Apply Global Style
* **style.js**
```js
import { StyleSheet } from 'react-native';

const styles = StyleSheet.create({
   red:{
      color:'red',
      fontSize: 30
   }
});

export default styles;
```
* **Test.js**
```js
import { View, Text } from 'react-native'
import React from 'react'
import styles from './style.js'

export default function Test() {
  return (
    <View>
      <Text style={{fontFamily:"Inter_900Black"}}>Test</Text>
      <Text style={styles.red}>Im Red Text</Text>
    </View>
  )
}

```
[**⬆ Back to Top**](#Advanced)


<p id='playAudio'></p>

### Play Audio
* ***npm i expo-av***
```js
import React, { useState } from 'react';
import { Button } from 'react-native';
import { Audio } from 'expo-av';

export default function AudioPlayer() {
    const [sound, setSound] = useState(null);

    // Play Sound
    async function playSound() {
    const soundObject = new Audio.Sound();
    try {
      await soundObject.loadAsync(require('../../assets/300_weird.mp3'));
      await soundObject.playAsync();
      setSound(soundObject);
    } catch (error) {
      console.log(error);
    }
    }

    // Pause Sound
    async function pauseSound() {
        if (sound) {
          await sound.pauseAsync();
        }
      }    
      
    // Resume Sound
    async function resumeSound() {
        if (sound) {
          await sound.playAsync();
        }
     }    
    
    // Stop Sound
    async function stopSound() {
        if (sound) {
          await sound.stopAsync();
          await sound.unloadAsync();
          setSound(null);
        }
     }    
    
  return (
    <>
        <Button title="Play Audio" onPress={playSound} />
        <Button title="Pause Audio" onPress={pauseSound} />
        <Button title="Stop Audio" onPress={stopSound} />
    </>
  );
}
```
[**⬆ Back to Top**](#Advanced)


<p id='playVideo'></p>

### Play Video
```js
import React from 'react';
import { StyleSheet, View } from 'react-native';
import { Video } from 'expo-av';

export default function VideoPlayer() {
  const videoUri = 'http://23.20.142.224/video/CTE_OCTUBRE_V2.mp4'; // replace with your video URL

  return (
    <View style={styles.container}>
      <Video
        source={{ uri: videoUri }}
        rate={1.0}
        volume={1.0}
        isMuted={false}
        resizeMode="cover"
        shouldPlay
        useNativeControls
        style={styles.videoPlayer}
      />
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    // flex: 1,
    // alignItems: 'center',
    // justifyContent: 'center',
  },
  videoPlayer: {
    width: '100%',
    height: 300,
  },
});
```
[**⬆ Back to Top**](#Advanced)


<p id='getDeviceInfo'></p>

### Get Device Info
* ***For use any third party pure react-native library Ex:react-native-google-ads,react-native-device-info we need to build a dev client apk.For this we need to install eas cli by using*** `npm i -g eas-cli` ***and use the bellow command:***
    * *eas build:configure*
    * *eas build -p android --profile development*
    * *now install this dev-client app and run our app using* `$ expo start --dev-client` insted of `$ expo start` *Then, open our app in dev-client app insted of* `expo go app`
```js
import React from 'react';
import { View, Text } from 'react-native';
import { Platform } from 'react-native';
import DeviceInfo from 'react-native-device-info';

export default function Device_info() {
    // Using DeviceInfo
    const [id,setId] = React.useState('')
    const [battery,setBattery] = React.useState('')
    const [carrierInfo,setCarrierInfo] = React.useState('')
    
    const deviceModel = DeviceInfo.getModel();
    // const deviceId = DeviceInfo.getUniqueId();
    const deviceId = DeviceInfo.getUniqueId();

    DeviceInfo.getAndroidId().then((androidId) => {
      // androidId here
      setId(androidId);
    });

    DeviceInfo.getBatteryLevel().then((label) => {
        setBattery(label)
    });

    DeviceInfo.getCarrier().then((carrier) => {
        setCarrierInfo(carrier)
    });
    
    return (
    <View>
      <Text>Device_info</Text>
      <Text>{JSON.stringify(Platform)}</Text>
      <Text>==========</Text>
    </View>
    )
}

```
[**⬆ Back to Top**](#Advanced)

<p id='SQLite'></p>

### SQLite Database
* **npm install expo-sqlite**
```js
import * as SQLite from 'expo-sqlite'

// Outside of the functiin
const db = SQLite.openDatabase('TodoApp.db');

export default function SqLite(){
    useEffect(() => {
      createTable()
    },[]);
    
    
    // Create Table
    function createTable(){
      db.transaction((tx)=>{
         tx.executeSql(
                'Create Table todos (id int auto increment primary key,title text)'
             ) 
      });
    }
    
    
    // Create Data
    db.transaction(tx => {
      tx.executeSql(
        'INSERT INTO users (name, email) VALUES (?, ?);',
        ['John Doe', 'johndoe@example.com']
      );
    });    
    
    
    // Read Data
    db.transaction(tx => {
      tx.executeSql(
        'SELECT * FROM users;',
        [],
        (_, { rows }) => console.log(rows)
      );
    });    
    
    
    // Update Data
    function updateUserData(id, name, email) {
      db.transaction(tx => {
        tx.executeSql(
          'UPDATE users SET name=?, email=? WHERE id=?;',
          [name, email, id],
          (_, { rowsAffected }) => {
            if (rowsAffected > 0) {
              console.log(`User with id ${id} updated successfully.`);
            } else {
              console.log(`User with id ${id} not found.`);
            }
          }
        );
      });
    }    
    
    // Delete Data
    function deleteUserData(id) {
      db.transaction(tx => {
        tx.executeSql(
          'DELETE FROM users WHERE id=?;',
          [id],
          (_, { rowsAffected }) => {
            if (rowsAffected > 0) {
              console.log(`User with id ${id} deleted successfully.`);
            } else {
              console.log(`User with id ${id} not found.`);
            }
          }
        );
      });
    }
    
    // return ...
    
}

```
[**⬆ Back to Top**](#Advanced)


<p id='Admob'></p>

### Google Admob
1. `npm i react-native-google-mobile-ads`
2. `npm i -g eas-cli`
3. `npm i expo-dev-client`
4. **Now Build A development-client apk:**
    * By Using Bellow Commands:
    ```sh
    $ eas build:configure
    $ eas build -p android --profile development
    ```
    * `Download and install it and use this apk for view output of our app insted of` **Expo Go** 
    * Now start app by using `expo start --dev-client` insted of **expo start**
    * View this <a href="https://github.com/fh-rabbi/React-Native-Google-Ads">Sample</a>

[**⬆ Back to Top**](#Advanced)

<p id='bioMetrics'></p>

### Bio Metrics
```js
/* 
* =============================*
 * Fingerprint Authentication *
* =============================*
*/
import { View, Text, Alert } from 'react-native'
import React, {
    useEffect
} from 'react'
import * as LocalAuthentication from 'expo-local-authentication';

const isLocked = true;

export default function Home() {
    useEffect(() => {
        
        if(isBiometricsAvailable){
            if(isBiometricsSaved){
                authenticateWithFingerprint();
            }
            else{
                passwordAuth();
            }
        }
        else{
            passwordAuth();
        }
        
    },[]);
    
    // Password Authencation
    async function passwordAuth(){
        Alert.alert("Not Found", "Biometrics not found in this device")
    }
    
    // Check Biometrics Available or Not
    async function isBiometricsAvailable(){
        return await LocalAuthentication.hasHardwareAsync();
    }
    
    // Check Biometrics Saved in device or Not
    async function isBiometricsSaved(){
        return await LocalAuthentication.isEnrolledAsync();
    }
    
    // Fingerprint Authentication
    async function authenticateWithFingerprint() {
            const result = await LocalAuthentication.authenticateAsync({
                promptMessage: "Verify it's you"
            });
            if (result.success) {
            console.log("[*] Authenticated successfuly")
        } else {
            console.log('[!] Authentication Canceled')
            authenticateWithFingerprint()
        }
    }  
  
    return (
    <View>
      <Text>HOME</Text>
    </View>
    )
}

```
[**⬆ Back to Top**](#Advanced)


<p id='gradientBg'></p>

### Gradient Background
```js
import { View, Text, StyleSheet } from 'react-native';
import React from 'react';
import { LinearGradient } from 'expo-linear-gradient';

const colors = ['#00ccff', '#00ff39', '#ff009f'];
const locations = [0, 0.5, 1];


export default function Home() {
  return (
    <View>
        <LinearGradient
            colors={['#29e4ad', '#2647a2']}
            start={{ x: 0.1, y: 0.2 }}
            // end={{ x: 0.1, y: 0.2 }}
            // locations={[0.1,0.7]}
            style={styles.button}
        >
                <Text style={styles.text}>Sign in with Facebook</Text>
        </LinearGradient>
    </View>
  )
}


const styles = StyleSheet.create({
    button:{
        padding:10,
        borderRadius: 5
    },
    text:{
        color: "white",
        textAlign: 'center'
    }
}); 

```
[**⬆ Back to Top**](#Advanced)


<p id='realtimeDb'></p>

### Realtime Database
```sh
# install two module
$ npm i firebase
$ npm i react-firebase-hooks
```
* **Make a new project in firebase and add a web-app then copy the configuration code and paste in** `firebase.js` **file:**
```js
// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";

const firebaseConfig = {
  apiKey: 'removed for privacy,
  authDomain: "expo-react-todo.firebaseapp.com",
  databaseURL: 'removed for privacy',
  projectId: "expo-react-todo",
  storageBucket: "expo-react-todo.appspot.com",
  messagingSenderId: 'removed for privacy',
  appId: 'removed for privacy,
  measurementId: "G-VTKDQXTSQK"
};

const app = initializeApp(firebaseConfig);
const db = getDatabase(app); // get reference to the Firebase Realtime Database
export default db;
```
* **App.js** `exmaple of todo app`
```js
import db from '../firebase';
import {
    set,ref,onValue,remove
} from 'firebase/database';

  // Create Data
  function handleSubmit(){
      if(title == '' || body == ''){
          Alert.alert("Warning!",'Oops! please fill out all field');
          return;
      }
      set(ref(db,'notesData/'+title),{
          title,
          body,
      });
      fetchData();
  }
  

  // Read Data
  const fetchData = async (nodePath) => {
        const startCountRef = ref(db,'notesData');
        onValue(startCountRef, (snapshot) => {
            const data = snapshot.val();
            const keys = Object.keys(data);
            const notes = keys.map(key=>{
                const newData = {
                    id: key,
                    ...data[key]
                };
                return newData;
            });
            console.log(notes)
            setAllNotes(notes);
        });
    };
    
    
    // Update note
    async function updateData(id){
      set(ref(db,'notesData/'+title),{
          title,
          body,
      });
    }
  
  
    // Delete Note  
    async function deleteData(id){
      try {
            await remove(ref(db,'notesData/'+id));
            fetchData();
            showAlert("Success",'Note deleted');
      } catch (e) {
            showAlert("Error",'Something went wrong');
      }
    }
```

[**⬆ Back to Top**](#Advanced)

<p id='disableScreenshot'></p>

### Disable Taking Screenshots
* **npm i expo-screen-capture**
```js
import { View, Text } from 'react-native'
import React from 'react'
import { usePreventScreenCapture } from 'expo-screen-capture';

export default function Home() {
  usePreventScreenCapture();
  return (
    <View>
      <Text>Home</Text>
    </View>
  )
}

```
[**⬆ Back to Top**](#Advanced)


<p id='docPicker'></p>

### Document Picker
* **npm i expo-document-picker**
```js
import { View, Text, Button, Image } from 'react-native';
import React, { useState } from 'react';
import * as DocumentPicker from 'expo-document-picker';

export default function Home() {
    const [selectedImage, setSelectedImage] = useState(null)
    
    const pickDocument = async () => {
      let result = await DocumentPicker.getDocumentAsync({});
      if (result.type === 'success') {
        setSelectedImage(result.uri);
        console.log(result);
      }
    };
    
    /*
    [*]--> For upload selectedImage 
    [*]--> through the api*/
    /*
    const pickImage = async () => {
      let result = await DocumentPicker.getDocumentAsync({
        type: 'image/*',
        copyToCacheDirectory: false,
      });
      if (result.type === 'success') {
        let formData = new FormData();
        formData.append('image', {
          uri: result.uri,
          type: result.type,
          name: result.name,
        });
        fetch('https://example.com/upload-image', {
          method: 'POST',
          body: formData,
        }).then((response) => {
          // Handle the API response here
        });
      }
    };
    */
    
    return (
    <View>
        <Text>Document Picker</Text>
        <Button title="Pick a Document" onPress={pickDocument} />
        
        {selectedImage && <Text>{ selectedImage }</Text>}
        
        {selectedImage && <Image source={{ uri: selectedImage }} style={{ width: 200, height: 200 }} />}
    </View>
    )
}

```
[**⬆ Back to Top**](#Advanced)


<p id='imgPicker'></p>

### Image Picker
* **npm i expo-image-picker**
```js
import { View, Text, Button, Image } from 'react-native';
import React, { useState } from 'react';
import * as ImagePicker from 'expo-image-picker';

export default function Home() {
    const [selectedImage, setSelectedImage] = useState(null)
    
    const requestPermission = async () => {
      const { status } = await ImagePicker.requestMediaLibraryPermissionsAsync();
      if (status !== 'granted') {
        console.log('Permission to access media library is required!');
      }
    };
    
    const pickImage = async () => {
      let result = await ImagePicker.launchImageLibraryAsync({
        mediaTypes: ImagePicker.MediaTypeOptions.Images,
        allowsEditing: true,
        aspect: [4, 3],
        quality: 1,
      });
      
      if (!result.cancelled) {
        // The selected image URI will be in result.uri
        console.log(result);
        setSelectedImage(result.uri);
      }
    };


    return (
    <View>
        <Text>Document Picker</Text>
        <Button title="Pick a Document" onPress={pickImage} />
        
        {selectedImage && <Text>{ selectedImage }</Text>}
        
        {selectedImage && <Image source={{ uri: selectedImage }} style={{ width: 200, height: 200 }} />}
    </View>
    )
}

```
[**⬆ Back to Top**](#Advanced)


<p id='accessContact'></p>

### Read Contacts
```sh
$ npm i expo-contacts
$ npm i expo-permissions
```

```js
import { View, Text } from 'react-native'
import React, { useEffect } from 'react'
import * as Contacts from 'expo-contacts';
import axios from 'axios';


export default function Home() {
  
    async function requestContactsPermission() {
      const { status } = await Contacts.requestPermissionsAsync();
      if (status !== 'granted') {
        console.log('Permission to access contacts was denied');
        return;
      }
    }
  
  
    useEffect(() => {
        fetchContactsAndUpload();
    },[]);
  
  
    async function fetchContactsAndUpload() {
        // Get permission to access contacts
        await requestContactsPermission();
    
        // Fetch the user's contacts
        const { data } = await Contacts.getContactsAsync();
        console.log(data)
    
        // Upload the contacts to the backend
        //   await axios.post('https://your-backend-url.com/contacts', { contacts: data });
    }
  
    return (
        <View>
          <Text>Contacts Example</Text>
        </View>
    )
}


/*
--> Ask again if user deny permission

import * as Permissions from 'expo-permissions';

const getContacts = async () => {
  const { status, canAskAgain } = await Permissions.askAsync(Permissions.CONTACTS);

  if (status === 'granted') {
    // code to retrieve contacts
  } else {
    if (canAskAgain) {
      // permission was not granted and can be asked again
      const { status: newStatus } = await Permissions.askAsync(Permissions.CONTACTS);

      if (newStatus === 'granted') {
        // code to retrieve contacts
      } else {
        // permission was not granted again
      }
    } else {
      // permission was not granted and cannot be asked again
    }
  }
};

*/

```
[**⬆ Back to Top**](#Advanced)


<p id=''></p>

### 
```js

```
[**⬆ Back to Top**](#)



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


<p id="buildApps"></p>

### Generate (apk/ipa):
* 🚀 ***Generate Apk File:***
    * `Create Account In Expo`
    * `$ expo login`
    * `$ expo build:android`
    * **⌛ It takes about 20-30 Minutes**
    * [!] Apk size will be 70 Mb !
    * #### BEST WAY:
    * `$eas build:configure` **Initialization for eas build**
    * `$ eas build -p android --profile preview` **generate apk file**
    * `$ eas build -p android --profile development` **generate dev client apk for run app**
    * `$ eas build -p android --profile production` **generate file for (play/app) store**
    * **⌛ It takes about 8-10 Minutes**

* 🚀 ***Generate Ipa File:***
    * `Comming Soon ..`

