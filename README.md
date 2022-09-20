<h1 align='center'>REACT NATIVE</h1>

### `🤔 What is React-Native?`

> **React Native is a cross-platform mobile application development framework that Facebook created in 2015. React Native uses JavaScript as the underlying programming language, and it aims to help developers build native mobile apps for both Android and iOS devices with a single codebase.**

### `🤔 What Is Cross-Platform Development?`

> **Cross-platform development is the art of writing software that runs on different platforms; you write your codebase once and share it across different platforms. Cross-platform development provides you with a broad target audience since you have various options for running your codebase. For example, one app can be shared across both Android and iOS devices, resulting in a broader user base.**

### `🤔 What does meaning native apps?`

> **The term native app development refers to building a mobile app exclusively for a single platform. The app is built with programming languages and tools that are specific to a single platform. For example, you can develop a native Android app with Java or Kotlin and choose Swift and Objective-C for iOS apps.**

### `🤔 What is hybrid app?`

> **Hybrid apps combine both web applications created for web browser and native applications that are designed for a particular platform and have to be installed on a device.**

### `✨ All About React-Native:`
* https://code.tutsplus.com/tutorials/what-is-react-native--cms-38028

### 🚨 `PREREQUISITES:`
* ***Html***
* ***Css***
* ***Javascript***
* ***React.js***

---

<h1 align='center'>Table Of Contents</h1>

### 💡 `Fundamentals:`

* [Setup React Native App]()
* [View,Text]()
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
* [Header Styling]()
* [Link]()
* [Async Storage]()
* [Activity Indicator]()
* [Web View]()
* [Styling]()
* [AsyncStorage]()
* [SQLite Database]()
* [Alert & Toast Message]()
* [Modal]()

* `React.js Hooks in React Native:`
   * `useState`
   * `useEffect`

### 💡 `Navigation:`
* [Stack Navigator]()
* [Tab Navigator]()
* [Drawer Navigator]()
* [useNavigate Hook]()
* [Passing Data Between Screen]()
* []()

### 🚀 `Generate Apk File:`
* `Create Account In Expo`
* `$ expo login`
* `$ expo build:android`
* ***⌛ Wait 20-30 Minutes***

---

<h1 align='center'>Fundamentals</h1>

### ✨ Setup React Native App:
```bash
$ npm i expo
$ expo init my-app
```
### ✨  View,Text:
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
### ✨  Buttons:
```js
import {Button} from 'react-native';

const Demo = () => {
   return(
      <Button
         title=''
         onPress={}
      >
         Open Link
      </Button>
   );
};

export default Demo;
```
### ✨  Touchables:
```js
import {TouchableOpacity} from 'react-native';

const Demo = () => {
   return(
      <TouchableOpacity
         onPress={}
      >
         <Text>Im A Button</Text>
      </TouchableOpacity>
   );
};

export default Demo;
```
### ✨  FlatList:
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
         />
      </View>
   );
};

export default Demo;
```
### ✨  Section List:
```js

```
### ✨  ScrollView:
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
### ✨  Image:
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
### ✨  Custom Fonts:
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
### ✨  Icons:
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
### ✨  Text Input:
```js
import {View,TextInput} from 'react-native';
import { FontAwesome5 } from '@expo/vector-icons';

const Demo = () => {
   return(
      <View>
         <TextInput
            onChangeText={}
            value={}
         />
      </View>
   );
};

export default Demo;
```
### ✨  Switch:
```js

```
### ✨  StausBar:
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
### ✨  Header Styling: 
```js

```
### ✨  Link:
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
### ✨  :
```js

```

<h1 align='center'>Navigation</h1>