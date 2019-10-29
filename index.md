<title>1Byte Homepage</title>
<div style=" height: 100%; left: 0; position: fixed; top: 0; width: 100%; z-index: -2; background-image: url(https://lh5.googleusercontent.com/proxy/T67n3enEs3xAxEDeRSnpECTqNroeHtO7YL4PKvpRxX9vysbp0MAWBQWAo6SHAXAZy6HHuBfxPWsxLyHMYhamcQntN4xyOCF6d1PqFNzsAGMcfVuKXA=s0-d); background-size: 700px 825px; "></div><div style=" background: rgba(0, 0, 0, 0.4) url(//4.bp.blogspot.com/-iO_ZWkwPW8A/Uz4dkFw4p4I/AAAAAAAABxo/KzpIdP8czxQ/s320/overlay.png) repeat; height: 100%; left: 0; position: fixed; top: 0; width: 100%; z-index: -1;background-size: 100px 100px;"></div>
<link href="https://fonts.googleapis.com/css?family=Staatliches&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css?family=Tajawal&display=swap" rel="stylesheet">
<link rel="shortcut icon" type="image/png" href="https://1.bp.blogspot.com/-iEbKgTfWPPg/Xbg7n2hEYKI/AAAAAAAAGUI/a1SdKJEPhmwk9wA61b-uW6uFUNdX-uYJACLcBGAsYHQ/s1600/logo-s.png">
<div style="padding: 3px;text-align:center;position:fixed;
    height:40px;
    background-image: linear-gradient(15deg, #b30202, #1d0303);
    width: 100%;
    left: 0px;
    top: 0px;
    opacity: 0.8;
    border-bottom: 1px solid #656464;
    box-shadow: 2px 2px 5px #000000;
    background: #4c0101;"><img src="https://2.bp.blogspot.com/-fLDN3fxMkfI/Xbi0ZObnmwI/AAAAAAAAGUY/_0f4n9o35-oEECycSGr-zupANKAkH_GfQCLcBGAsYHQ/s1600/logo-white.png" class="logo"><style>
    .logo{height: 32px;
    margin: -10px;
    margin-left: 3px;}
    .logo:hover{opacity: 0.5;white;transition: all .4s ease;
-webkit-transition: all .4s ease;}.logo:active{opacity: 0.5;white;transition: all .4s ease;
-webkit-transition: all .4s ease;}
    .main-content pre{direction: ltr;}.main-content h2{color: #991515 !important;}.main-content h3{color: #991515 !important;}.main-content{border-radius: 15px 15px 0 0;padding-top: 4px;font-family: 'Tajawal', sans-serif;direction: rtl;box-shadow: 1px 1px 3px #ccc;
    margin-top: 65px;
    background: white;}
    .page-header{
    margin-top: 17px;
    padding: 0px !important;
    background: #000000;
    position: absolute;
    z-index: 1;
    border-radius: 5px;
    opacity: 0.5;
    top: 47px;
    border: 2px solid #ababab;
    background-image: url(https://1.bp.blogspot.com/-iEbKgTfWPPg/Xbg7n2hEYKI/AAAAAAAAGUI/a1SdKJEPhmwk9wA61b-uW6uFUNdX-uYJACLcBGAsYHQ/s1600/logo-s.png);
    background-repeat: no-repeat;
    background-size: 400px 400px;}.body{background: #f5f5f5;}.btn{padding: 0px;}.project-name{font-size:24px !important;font-family:'Staatliches',cursive;color: #FFFFFF;font-size: 16px;}
.a:hover{text-decoration:none;}.title{color: white;
    text-decoration: none !important;
    padding-right: 5px;
    padding-left: 5px;
    border-radius: 5px;
    padding: 5px;
    font-size: 19px;}
.title:link{white;
    text-decoration: none !important;}
.title:visited{white;
    text-decoration: none !important;}
.title:hover{white;transition: all .4s ease;
-webkit-transition: all .4s ease;
    text-decoration !important: none;background: #f1efef2e;}
.title:active{white;
    text-decoration !important: none;}</style>
  <a href=""><font class="title">الرئيسية</font></a>
    <a href=""><font class="title">عن القناة</font></a>
    <a href=""><font class="title">صفحتنا على الفيسبوك</font></a>
    
    </div>

## الصفحة الرئيسية


### مثال لكود برمجي



```markdown
#include <LiquidCrystal.h>

#include <Keypad.h>
int led = 10;int a,b,c,d;

const byte ROWS = 4; //four rows
const byte COLS = 4; //three columns
char keys[ROWS][COLS] = {
  {'1','2','3','A'},
  {'4','5','6','B'},
  {'7','8','9','C'},
  {'*','0','#','D'}
};

LiquidCrystal lcd(A0, A1, A2, A3, A4, A5);

byte rowPins[ROWS] = {2, 3, 4, 5}; //connect to the row pinouts of the keypad
byte colPins[COLS] = {6,7,8,9}; //connect to the column pinouts of the keypad

Keypad keypad = Keypad( makeKeymap(keys), rowPins, colPins, ROWS, COLS );

void setup(){
  Serial.begin(9600);
  pinMode(led, OUTPUT);   
  lcd.begin(16,2);
 
}
  
void loop(){
  
  
  
  char key = keypad.getKey();
    // just print the pressed key
   if (key){
    Serial.println(key);lcd.print(key); delay(300);
  } 
  
  // this checkes if 4 is pressed, then do something. Here  we print the text but you can control something.
  if (key =='6'){a=1;}
  if (key =='8' and a == 1){b=1;}
  if (key =='9' and b == 1){c=1;}
  if (key =='1' and c == 1){digitalWrite(led,1);}
    
  
}
# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**خط غليظ** و _خط مائل_ و `كود` تكست

[Link](url) and ![Image](src)
```

//For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/zakariazaio/1Byte/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

