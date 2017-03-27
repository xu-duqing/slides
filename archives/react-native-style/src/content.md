# React Native 布局

- - -

### UI Style
## React Native

- - -

## 什么是UI布局？
元素、尺寸、位置 

- - -

## Flex
弹性布局方案

- - -

## 轴线
![](http://onhff7qaf.bkt.clouddn.com/0.png)

- - -

## flexDirection
{ row | row-reverse | column | column-reverse }

- - -

![](http://onhff7qaf.bkt.clouddn.com/1.png)

```javascript
diceBox:{ 

}
```

- - -

![](http://onhff7qaf.bkt.clouddn.com/2.png)

```javascript
diceBox:{ 
    flexDirection:'row' 
}
```

- - -

## flexWrap
{ nowrap | wrap}

- - -

![](http://onhff7qaf.bkt.clouddn.com/4.png)

```javascript
diceBox:{ 
    exWrap:'wrap'
 }
```

- - -

## justifyContent
{ flex-start | flex-end | center | space-between | space-around}

- - -

![](http://onhff7qaf.bkt.clouddn.com/5.png)

```javascript
diceBox:{ 
    justifyContent:'center'
 }
```

- - -

## alignItems
{ flex-start | flex-end | center | stretch}

- - -

![](http://onhff7qaf.bkt.clouddn.com/6.png)

```javascript
diceBox:{ 
    alignItems:'center'
 }
```

- - -

## alignSelf
{ auto | flex-start | flex-end | center | stretch}

- - -

![](http://onhff7qaf.bkt.clouddn.com/7.png)

```javascript
diceBox3:{ 

},
 diceBox3Dot2:{ 
    ignSelf:'center' 
}, 
diceBox3Dot3:{ 
    ignSelf:'flex-end' 
}
```

- - -

### padding | margin | position 
### border | flex | height | width

- - -

## Style
```javascript
const styles = StyleSheet.create({ 
    ceBox1:{ 
        ifyContent:'center', 
        alignItems:'center' 
        } 
    });

style={[styles.diceBox,styles.diceBox1]}
```

`node_modules/react-native/Libraries/StyleSheet`

- - -

```javascript
export default styles = StyleSheet.create({  
    box:{ 
        marginTop:Platform.OS === 'android'?50:60  
    }
 })
```

```javascript
const styles = StyleSheet.create({   
    box:{ 
        height:100,  
        ios:{  backgroundColor:'blue' },    
        android:{  backgroundColor:'red'} 
        } 
    }) 
```

- - -

## 单位
pt / px / dp / sp / ppi / dpi

- - -

### 套路：2px  = 1sp = 1pt
- @1x  —> mdpi  160ppi
- @2x  —> xhdpi  320ppi
- @3x  —> xxhdpi 480ppi

- - -

### Text | TextInput | Image  
### ListView | ScrollView 

- - -

## Text
```html
<Text style={styles.baseText}>  
 这里样式文本嵌套， 
    <Text style={styles.redText}>   红色   </Text>  
    <Text style={styles.blueText}>    蓝色   </Text> 
</Text>
```

![](http://onhff7qaf.bkt.clouddn.com/8.png)

- - -

## ART
React Native 矢量绘图库

- - -

![](http://onhff7qaf.bkt.clouddn.com/9.png)

- - -

# Thank you
