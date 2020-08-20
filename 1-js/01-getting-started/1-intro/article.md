# מבוא לג'אווהסקריפט
Let's see what's so special about JavaScript, what we can achieve with it, and which other technologies play well with it.\
בואו נראה מה כל כך מיוחד בג'אווהסקריפט, מה אפשר לעשות איתה, ועם אילו טכנולוגיות נוספות מסתדרות היא מסתדרת נהדר.

## מה זה ג'אווה סקריפט

*JavaScript* was initially created to "make web pages alive".\
*ג'אווהסקריפט* נוצרה במטרה "להחיות" את האינטרנט

The programs in this language are called *scripts*. They can be written right in a web page's HTML and run automatically as the page loads.\
קטעי התוכנה בשפה נקראים *סקריפטים*. הם יכולים להיכתב ישירות בHTML ולרוץ מיד כאשר העמוד עולה. 

Scripts are provided and executed as plain text. They don't need special preparation or compilation to run.
סקריפטים מסופקים ורצים כטקסט שהם. הם לא צריכים הכנות מיוחדות דוגמת [הידור](https://he.wikipedia.org/wiki/%D7%9E%D7%94%D7%93%D7%A8) כדי לרוץ.

In this aspect, JavaScript is very different from another language called [Java](https://en.wikipedia.org/wiki/Java_(programming_language)).\
במובן הזה, ג'אווהסקריפט שונה מאד משפה אחרת הנקראת [ג'אווה](https://he.wikipedia.org/wiki/%D7%92%27%D7%90%D7%95%D7%95%D7%94_(%D7%A9%D7%A4%D7%AA_%D7%AA%D7%9B%D7%A0%D7%95%D7%AA)).

```smart header="Why is it called <u>Java</u>Script?\ מדוע היא נקראת <u>ג'אווה</u>סקריפט?"
When JavaScript was created, it initially had another name: "LiveScript". But Java was very popular at that time, so it was decided that positioning a new language as a "younger brother" of Java would help.
כשג'אווהסקריפט נוצרה, היה לה שם אחר: "LiveScript" . אבל ג'אווה היתה מאד פופולרית בזמנו, אז הוחלט שהצגת השפה החדשה כאחיה הקטן של ג'אווה תועיל.\
But as it evolved, JavaScript became a fully independent language with its own specification called [ECMAScript](http://en.wikipedia.org/wiki/ECMAScript), and now it has no relation to Java at all.\
אבל עם התפתחות השפה, ג'אווהסקריפט נהייתה עצמאית לחלוטין עם מפרט סטנדרטים (ספציפיקציה) משלה, הנקרא [ECMAScript](http://he.wikipedia.org/wiki/ECMAScript), וכיום כבר אין לה שום קשר לג'אווה.
```

Today, JavaScript can execute not only in the browser, but also on the server, or actually on any device that has a special program called [the JavaScript engine](https://en.wikipedia.org/wiki/JavaScript_engine).\
כיום, ג'אווה סקריפט רצה לא רק על גבי הדפדפן, אלא גם על השרת, ולמעשה בכל מכשיר שמותקנת בו תוכנה מיוחדת הנקראת מנוע ג'אווהסקריפט

The browser has an embedded engine sometimes called a "JavaScript virtual machine".\
לכל דפדפן יש מנוע כזה שמוטמע בו, שיש שקוראים לו "מוכנה וירטואלית של ג'אווהסקריפט".

Different engines have different "codenames". For example:
- [V8](https://en.wikipedia.org/wiki/V8_(JavaScript_engine)) -- in Chrome and Opera.
- [SpiderMonkey](https://en.wikipedia.org/wiki/SpiderMonkey) -- in Firefox.
- ...There are other codenames like "Trident" and "Chakra" for different versions of IE, "ChakraCore" for Microsoft Edge, "Nitro" and "SquirrelFish" for Safari, etc.

למנועים שונים יש "שמות קוד" שונים. לדוגמה:\
- [V8](https://he.wikipedia.org/wiki/V8) -- מוטמע בכרום ואופרה
- [SpiderMonkey](https://en.wikipedia.org/wiki/SpiderMonkey) -- בפיירפוקס.
- יש שמות קוד נוספים, כמו "Trident" ו"Chakra" לגרסאות שונות של אינטרנט אקספלורר, "ChakraCore" בשביל מיקרוספוט אדג', "Nitro" ו- "SquirrelFish" בשביל סאפרי, וכו'.

The terms above are good to remember because they are used in developer articles on the internet. We'll use them too. For instance, if "a feature X is supported by V8", then it probably works in Chrome and Opera.\
כדאי לזכור את המונחים לעיל, מאחר ומשתמשים בהם במאמרים שונים באינטרנט הנוגעים לפיתוח. גם אנחנו נשתמש בהם. לדוגמה, אם "תכונה X נתמכת על ידי V8", אז כנראה שזה עובד בכרום ואופרה.

```smart header="How do engines work? \ איך מנועים עובדים?"

Engines are complicated. But the basics are easy.

1. The engine (embedded if it's a browser) reads ("parses") the script.
2. Then it converts ("compiles") the script to the machine language.
3. And then the machine code runs, pretty fast.

The engine applies optimizations at each step of the process. It even watches the compiled script as it runs, analyzes the data that flows through it, and further optimizes the machine code based on that knowledge.\\
מנועים הם דבר מסובך, אבל הבסיס פשוט וקל.
1. המנוע (המוטמע, אם מדובר בדפדפן) קורא ("מנתח") את הסקריפט.
2. אז הוא ממיר ("מהדר") את הסקריפט לשפת מכונה.
3. ואז קוד המוכנה רץ, די במהירות
```

## What can in-browser JavaScript do?

Modern JavaScript is a "safe" programming language. It does not provide low-level access to memory or CPU, because it was initially created for browsers which do not require it.

JavaScript's capabilities greatly depend on the environment it's running in. For instance, [Node.js](https://wikipedia.org/wiki/Node.js) supports functions that allow JavaScript to read/write arbitrary files, perform network requests, etc.

In-browser JavaScript can do everything related to webpage manipulation, interaction with the user, and the webserver.

For instance, in-browser JavaScript is able to:

- Add new HTML to the page, change the existing content, modify styles.
- React to user actions, run on mouse clicks, pointer movements, key presses.
- Send requests over the network to remote servers, download and upload files (so-called [AJAX](https://en.wikipedia.org/wiki/Ajax_(programming)) and [COMET](https://en.wikipedia.org/wiki/Comet_(programming)) technologies).
- Get and set cookies, ask questions to the visitor, show messages.
- Remember the data on the client-side ("local storage").
## מה יכול "ג'אווהסקריפט שבדפדפן" לעשות?
ג'אווהסקריפט נחשבת לשפת תכנות בטוחה. היא לא מספקת גישת low level לזיכרון או למעבד, מאחר והיא נוצרה לשימוש הדפדפן, שאינו זקוק לכך. 

היכולות של ג'אווהסקריפט תלויות באופן משמעותי בסביבה שהיא רצה בה. לדוגמה, [Node.js](https://he.wikipedia.org/wiki/Node.js) מספק פונקציות שמאפשרות לג'אווהסקריפט לקרוא/לכתוב קבצים באופן חופשי, לבצע בקשות מעל הרשת, וכו'.

כשהיא רצה על גבי הדפדפן, ג'אווהסקריפט יכולה לעשות את כל הקשור לשינוי דף האינטרנט, תקשורת עם המשתמש והשרת.

לדוגמה, בדפדפן, ג'אווהסקריפט מסוגלת:
- להוסיף HTML חדש לדף, לשנות תוכן קיים, ולשנות את העיצוב של הדף.
- להגיב לפעולות של המשתמש, לרוץ בלחיצת עכבר, בתזוזות סמן, בשימוש במקלדת. 
- לשלוח בקשות מעל הרשת לשרת מרוחק, להוריד או להעלות קבצים (מה שנקרא - [AJAX](https://he.wikipedia.org/wiki/AJAX_(%D7%AA%D7%9B%D7%A0%D7%95%D7%AA)) ו- COMET)
- לקרוא וליצור קבצי cookies, לשאול שאלות את הגולש, להציג הודעות.
-  לשמור נתונים אצל צד הלקוח ("local storage").
## What CAN'T in-browser JavaScript do?

JavaScript's abilities in the browser are limited for the sake of the user's safety. The aim is to prevent an evil webpage from accessing private information or harming the user's data.

## מה הוא <ins>לא</ins> יכול לעשות?

Examples of such restrictions include:
מספר דוגמאות למגבלותיה של ג'אווהסקריפט בדפדפן:
- JavaScript on a webpage may not read/write arbitrary files on the hard disk, copy them or execute programs. It has no direct access to OS functions.
- היא לא יכולה לקרוא או להעתיק קבצים שנמצאים בזיכרון הקשיח, לכתוב אליו, או להריץ תוכנות. אין לה שום גישה ישירה לפונקציות של מערכת ההפעלה 
    Modern browsers allow it to work with files, but the access is limited and only provided if the user does certain actions, like "dropping" a file into a browser window or selecting it via an `<input>` tag.
    דפדפנים מודרנים מאפשרים לה לעבוד עם קבצים, אבל הגישה מוגבלת לפעולות מסוימות, כמו "גרירה" של קובץ לתוך חלון דפדפן או בחירה בו באמצעות תג `<input>`.

    There are ways to interact with camera/microphone and other devices, but they require a user's explicit permission. So a JavaScript-enabled page may not sneakily enable a web-camera, observe the surroundings and send the information to the [NSA](https://en.wikipedia.org/wiki/National_Security_Agency).


    ישנן דרכים לתקשר עם המצלמה/מיקורפון ומכשירים נוספים, אבל הן דורשות את רשותו המפורשת של המשתמש. כלומר, דף שמאובזר בג'אווהסקריפט לא יוכל להפעיל חרישית מצלמת אינטרנט, לתצפת על הסביבה, ולדווח ל[NSA](הסוכנות_לביטחון_לאומי).


- Different tabs/windows generally do not know about each other. Sometimes they do, for example when one window uses JavaScript to open the other one. But even in this case, JavaScript from one page may not access the other if they come from different sites (from a different domain, protocol or port).

-   באופן כללי, כרטיסיות (או חלונות) לא יודעות אחת על השנייה. לפעמים הן כן, לדוגמה, כאשר חלון אחד משתמש בג'אווהסקריפט כדי לפתוח חלון אחר. אבל גם במקרה הזה, ג'אווהסקריפט מדף אחד לא יוכל לגשת לדף אחר אם הם שייכים לאתרים שונים. (דומיין שונה, פרוטוקול שונה, או פורט שונה).

    This is called the "Same Origin Policy". To work around that, *both pages* must agree for data exchange and contain a special JavaScript code that handles it. We'll cover that in the tutorial.

    זה נקרא "Same Origin Policy" ("מדיניות המקור המשותף"). כדי לעקוף את זה, *שני הדפים* חייבים להסכים לחילופי הנתונים ולהכיל קוד ג'ווהסקריפט מיוחד שינהל אותם. נכסה זאת במדריך.

    This limitation is, again, for the user's safety. A page from `http://anysite.com` which a user has opened must not be able to access another browser tab with the URL `http://gmail.com` and steal information from there.

    גם המגבלה הזו היא לביטחון המשתמש. לא יכול להיות שדף מ`http://anysite.com` שנפתח על ידי המשתמש יוכל לגשת ל`http://gmail.com` ולגנוב משם מידע. 

- JavaScript can easily communicate over the net to the server where the current page came from. But its ability to receive data from other sites/domains is crippled. Though possible, it requires explicit agreement (expressed in HTTP headers) from the remote side. Once again, that's a safety limitation.

- ג'אווהסקריפט יכולה לתקשר בקלות מעל הרשת עם השרת ממנו הגיע הדף הנוכחי. אבל היכולת שלה לקבל מידע מאתרים/דומיינים אחרים מוגבלת. אם כי אפשרית, הדבר מצריך הסכמה מפורשת (בHTTP headers) מהצד המרוחק. פעם נוספת - זוהי מגבלת ביטחון.


![](limitations.svg)

Such limits do not exist if JavaScript is used outside of the browser, for example on a server. Modern browsers also allow plugin/extensions which may ask for extended permissions.

הגבלות כגון זו אינן קיימות כשמשתמשים בג'אווהסקריפט מחוץ לשרת. דפדפנים מודרנים מאפשרים  גם פלאגינים/הרחבות, שעשויים לבקש הרשאות נוספות. 
## What makes JavaScript unique?
There are at least *three* great things about JavaScript:

```compare
+ Full integration with HTML/CSS.
+ Simple things are done simply.
+ Support by all major browsers and enabled by default.
```
JavaScript is the only browser technology that combines these three things.

That's what makes JavaScript unique. That's why it's the most widespread tool for creating browser interfaces.

That said, JavaScript also allows to create servers, mobile applications, etc.

## מה מייחד את ג'אווהסקריפט?

ישנם לפחות *שלושה* דברים נהדרים בנוגע לג'אווהסקריפט:
```compare
+ אינטריגציה מלאה עם HTML/CSS.
+ דברים פשוטים נעשים בפשטות.
+ נתמך על ידי כל הדפדפנים הגדולים ומאופשר כברירת מחדל.
```
## Languages "over" JavaScript

The syntax of JavaScript does not suit everyone's needs. Different people want different features.

That's to be expected, because projects and requirements are different for everyone.

So recently a plethora of new languages appeared, which are *transpiled* (converted) to JavaScript before they run in the browser.

Modern tools make the transpilation very fast and transparent, actually allowing developers to code in another language and auto-converting it "under the hood".

## שפות "על גבי" ג'אווהסקריפט

התחביר (syntax) של ג'אווהסקריפט אינו תואם לצרכים של כל אחד. אנשים שונים צריכים מאפיינים שונים.

זהו דבר צפוי, מאחר שלכל אחד יש פרויקטים שונים ודרישות שונות. 

אז לאחרונה אנו עדים לשפע של שפות חדשות, שמבצעות  *טרנס-קומפילציה* (מתרגמות) לג'אווהסקריפט לפני שהן רצות בדפדפן. 

Examples of such languages:

- [CoffeeScript](http://coffeescript.org/) is a "syntactic sugar" for JavaScript. It introduces shorter syntax, allowing us to write clearer and more precise code. Usually, Ruby devs like it.
- [TypeScript](http://www.typescriptlang.org/) is concentrated on adding "strict data typing" to simplify the development and support of complex systems. It is developed by Microsoft.
- [Flow](http://flow.org/) also adds data typing, but in a different way. Developed by Facebook.
- [Dart](https://www.dartlang.org/) is a standalone language that has its own engine that runs in non-browser environments (like mobile apps), but also can be transpiled to JavaScript. Developed by Google.

There are more. Of course, even if we use one of transpiled languages, we should also know JavaScript to really understand what we're doing.

דוגמאות לשפות כאלו:
- [CoffeScript](http://coffeescript.org/) היא "ציפוי של סוכר" מעל ג'אווהסקריפט. היא מביאה תחביר קצר יותר, ומאפשרת לנו לכתוב קוד באופן יותר בהיר ומדויק. בדרך כלל, היא חביבה אצל מפתחי Ruby.
- [TypeScript](http://www.typescriptlang.org/) מתרכזת בהוספת טיפוסיות נתונים קפדנית יותר במטרה לפשט את תהליך הפיתוח והתמיכה של מערכות מורכבות. היא מפותחת על ידי מיקרוסופט. 
- [FLOW](http://flow.org/) גם כן מוסיפה טיפוסי נתונים, אבל באופן אחר. מפותחת על ידי פייסבוק.
- [Dart](https://www.dartlang.org/) היא שפה בפני עצמה שרצה מחוץ לדפדפן (כמו אפליקציות לנייד), אבל יכולה גם להתרגם לג'אווהסקריפט. מפותחת על ידי גוגל.

יש עוד. אבל אפילו אם אנחנו משתמשים בשפה שעוברת טרנס-קומפילציה לג'אווהסקריפט, כמובן שעלינו לדעת ג'אווהסקריפט כדי באמת להבין מה אנחנו עושים.

## Summary

- JavaScript was initially created as a browser-only language, but is now used in many other environments as well.
- Today, JavaScript has a unique position as the most widely-adopted browser language with full integration with HTML/CSS.
- There are many languages that get "transpiled" to JavaScript and provide certain features. It is recommended to take a look at them, at least briefly, after mastering JavaScript.

## סיכום
- ג'אווהסקריפט נוצרה במקור כשפה המיועדת לדפדפן, אבל כיום היא בשימוש בסביבות רבות נוספות.
- כיום, ג'אווהסקריפט היא במעמד מיוחד כשפת הדפדפן המאומצת ביותר עם אינטרגציה מלאה עם HTML/CSS.
- ישנן שפות נוספות שמתרגמות לג'אווהסקריפט ומספקות מאפיינים מסויימים. מומלץ להעניק להן מבט, לפחות קצר, אחרי שקונים שליטה בג'אווהסקריפט.