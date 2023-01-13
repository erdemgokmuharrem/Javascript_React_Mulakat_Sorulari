# Javascript_React_Mulakat_Sorulari

Selamlar ben Erdem, girdiğim ve başka mülakatlardan duyduğum soruları tek bir dökümanda toplamaya,chatGPT ile cevaplandırmaya çalıştım herhangi bir sorunuz olursa dilediğiniz zaman yazabilirsiniz. discord:erdemthedev#4444 & [Kampus Discord](https://discord.kamp.us/)

# 1.HTML dosyası içerisine js çağırma yöntemleri nelerdir ve nerede çağırmalıyız ?

HTML kodumuzun içine head ve body arasına <script> tagi içinde de yazabiliriz ya da 
Dışarıdan oluşturduğumuz js dosyasını html kodumuzun içinde çağırırız.(script src)
# 2.Semantic HTML nedir ?
Semantik HTML etiketleri Sayfadaki içeriğin hangi bölümü önemli, hangi kısım tamamlayıcı dolayısıyla öncelikli değil, hangi alan navigasyon için gibi soruların cevaplarının arama motorlarına bildirilmesini sağlayan HTML5, Google ve Bing gibi büyük arama motorları için önemli semantik ipuçları sağlayabiliyor. Ayrıca HTML5, arama motorlarına anlamlı bilgi iletilmesinin yanı sıra multimedya kullanımını da kolaylaştırarak ekstra uzantılara ihtiyaç duymadan interaktif sayfalar hazırlamanıza olanak sağlıyor.

# 3.Const — let — var farkları nelerdir ?

## VAR=>  ile tanımlanan değişkenler daha sonra değiştirilebilir.
	Kodun herhangi bir yerinde kullanılabilir ve birden fazla kullanılabilir
	Var ile tanımlanan değişlenler function scopetur yani fonksiyon içerisinde var kullanılarak tanımlanmış değişkenlere fonksiyon dışından erişilemez.
## LET = > ile tanımlanmış değişkenlere sadece tanımlandığı kapsamda ulaşılabilir yani block scope {}
	Süslü parantezin içerisidir , sonradan tekrar değiştirilebilir, aynı kapsam içerisinde sadece bir sefer tanımlanabilir tekrar tanımlanırsa kod hata verir.
## CONST => const ile tanımlanmış bir değişken let kullanımında olduğu gibi tanımlandığı kapsam (block scope) içerisinden erişilebilir ve bunun dışından erişimler 	sağlanmaz. const kelimesi aslında Constant yani Sabit anlamını taşımaktadır . Kullanıldığı kapsam içerisinde sabittir ve değiştirilemez .
# 4. Javascriptte hangi veri tipleri kullanılır
Javascript' de veri tutmak için kullandığımız javascript veri tiplerini 2 ayrı grupta ele alabiliriz. Basit Veri Tipleri: String, Number, Boolean ve undefined. Referans Tipler: Dizi, Nesne, Fonksiyon ve null veri tipleridir.

	# 5.Reference ve Primitive type arasındaki farklar.
	Eğer bir metoda primitive type bir parametre gönderiyorsak bu değer kopyalanarak gider. Metodun içinde değer değiştirilse bile orijinal değerde bir değişiklik 		olmaz. Reference type bir veri herhangi bir metoda parametre geçildiğinde nesne reference olarak gönderilir.
# 6. { }=== { } ne döner
JavaScript'te, {} === {} karşılaştırması "false" dönecektir. Çünkü bu iki nesne farklı bellek adreslerinde yer alırlar ve JavaScript bu iki nesnenin farklı olmasını sonucu olarak "false" döner. Eğer nesnelerin içerikleri aynı ise bu karşılaştırma için Object.is() veya lodash gibi kütüphanelerin "isEqual" metodları kullanılabilir.
# 7. { }== { } ne döner 
Ayrıca eşitlik operatörü (==) birçok durumda veri tiplerini dönüştürdükten sonra karşılaştırma yaparken,(===) eşitlik operatörü veri tiplerini dönüştürmeden karşılaştırma yapar.

# 8. Javascript ile dom elementlerine erişim methodları nelerdir ?
JavaScript ile DOM (Document Object Model) elementlerine erişmek için birkaç farklı yol vardır. Bunlar arasında en yaygın olanlar:
document.getElementById(): Bu metod, belirtilen id'ye sahip bir elementi döndürür. Örnek: var myElement = document.getElementById("myId");
document.getElementsByTagName(): Bu metod, belirtilen etiket adına sahip tüm elementleri döndürür. Örnek: var listItems = document.getElementsByTagName("li");
document.querySelector(): Bu metod, belirtilen CSS sorgusuna uyan ilk elementi döndürür. Örnek: var myElement = document.querySelector("#myId .myClass");
document.querySelectorAll(): Bu metod, belirtilen CSS sorgusuna uyan tüm elementleri döndürür. Örnek: var listItems = document.querySelectorAll("li.active");
element.getAttribute() : Bu metod, belirtilen özellik değerini döndürür. Örnek : var myAttribute = myElement.getAttribute("href");

# 9.javascript hoisting kavramını açıklayın
JavaScript içinde "hoisting" (yukseltme) kavramı, deklarasyonların çalışma zamanında yukarı taşınmasına denir. Bu, belirli bir kod bloğunda tanımlanan deklarasyonların, o kod bloğunun üst kısmına taşınmasına neden olur. Bu, deklarasyonların kod bloğunun herhangi bir yerinde kullanılabileceği anlamına gelir.
Örneğin, aşağıdaki kod bloğunda, "x" değişkeni tanımlanmadan önce kullanılmıştır:
console.log(x); // undefined var x = 5; 
Ancak JavaScript, bu kod bloğunu çalıştırırken, deklarasyonu yukarı taşıyarak aşağıdaki şekilde işlem yapar:
var x; console.log(x); // undefined x = 5; 
Bu nedenle, bu kod bloğunda "x" değişkeni tanımlanmadan önce kullanılmış olsa da, JavaScript hoisting sayesinde "x" değişkeni tanımlanmış olarak kabul eder ve "undefined" döndürür.
Ancak JavaScript sadece deklarasyonları yukarı taşır, atamaları taşımaz. Örneğin aşağıdaki kod bloğu hata verir:
console.log(x); // ReferenceError: x is not defined let x = 5; 
Bu nedenle, JavaScript'de hoisting sadece var ve function tipinde deklarasyonlar için geçerlidir.
# 10. Local storage ve Session Storage Kavramlarını açıklayın
JavaScript içinde "Local Storage" ve "Session Storage" kavramları, web tarayıcıları tarafından sağlanan veri depolama mekanizmalarıdır. Bu mekanizmalar, web uygulamaları için kullanıcı tarafından girilen verileri veya uygulamanın tarafından oluşturulan verileri depolamak için kullanılır.
"Local Storage": Bu mekanizma, verileri tarayıcının kapatılmasına kadar saklar. Bu, kullanıcının tarayıcıyı kapattıktan sonra bile uygulamanın verilerine erişebilmesini sağlar. Local Storage verileri depolamak için "localStorage" objesini kullanır. Örneğin, aşağıdaki kod bloğu "myData" adlı bir veriyi Local Storage'a kaydeder:
Session Storage": Bu mekanizma, verileri tarayıcının kapatılmasına veya sekme kapatılmasına kadar saklar. Bu, kullanıcının tarayıcıyı veya sekmeyi kapattıktan sonra verilerin kaybolmasını sağlar. Session Storage verileri depolamak için "sessionStorage" objesini kullanır. Örneğin, aşağıdaki kod bloğu "myData" adlı bir veriyi Session Storage'a kaydeder:

	# 11. Local Storage’da hangi tür veri tutabiliriz.Eğer elimizdeki veri uygun değilse ne yapabiliriz ?
Local Storage, web tarayıcıları tarafından sağlanan veri depolama mekanizmasıdır. Bu mekanizma, string veri tipinde verileri depolamak için kullanılır. Bu nedenle, Local Storage içinde sadece string veri tipinde verileri depolayabilirsiniz. Örneğin, sayılar, nesneler veya diziler gibi diğer veri tiplerini depolamak için dönüştürmeniz gerekir.
Elimizdeki veri uygun değilse, verileri dönüştürebilir veya başka bir veri depolama mekanizması kullanabilirsiniz. Örneğin, JSON.stringify() metodunu kullanarak nesneleri veya dizileri string veri tipine dönüştürebilirsiniz.

	let myData = {name: "John", age: 25}; localStorage.setItem("myData", JSON.stringify(myData));
# 12.Arrow Function nedir, sağladığı kolaylıklar nelerdir.
JavaScript'te, "arrow function" (ok işaretli fonksiyon) bir fonksiyon tanımı şeklidir. Bu fonksiyonlar, daha kısa ve okunaklı kod yazmak için kullanılır. Arrow function'lar, function anahtar kelimesi yerine => operatorü kullanılarak tanımlanır.
Aşağıdaki örnekte, "myFunction" adlı bir fonksiyon tanımlanmıştır:
function myFunction(a, b) { return a + b; } 
Bu fonksiyonu arrow function ile yazmak için
let myFunction = (a, b) => { return a + b; } 
Arrow function'lar sağladığı kolaylıklar arasında:
Kodun daha kısa ve okunaklı olmasıdır.
- Arrow function'lar, "this" anahtar kelimesinin çalışma zamanında tanımlanmasını sağlar.
- Arrow function'lar, "return" anahtar kelimesini atlayarak daha kısa kod yazmanıza olanak tanır.
- Arrow function'lar, closure'ların oluşmasını kolaylaştırır. Bu closure'lar yerel değişkenlere erişim sağlar.
- Arrow function'lar güncel bir javascript sürümünde kullanılması önerilir, çünkü eski javascript sürümlerinde çalışmayabilir.
Bu kolaylıklar ile arrow function'lar ile kod yazarken daha okunaklı, daha kısa ve daha mantıklı hale getirebilirsiniz.
# 13. Higher order functionlar nedir,nerelerde kullanırız 
JavaScript'te "higher-order function" (yüksek-seviye fonksiyon), bir fonksiyonun argüman olarak veya döndürdüğü değer olarak başka bir fonksiyonu kullanmasını ifade eder. Yüksek seviye fonksiyonlar, fonksiyonların parametre olarak veya döndürdüğü değer olarak fonksiyonları kullanmasını sağlar. Bu fonksiyonlar ile kodunuz daha esnek ve modüler hale getirilir.
İterasyon işlemleri: Örneğin, dizilerdeki elemanları gezmek için kullanılan "forEach", "map", "filter" gibi fonksiyonlar yüksek seviye fonksiyonlardır.
Asenkron işlemler: Örneğin, bir promise'in sonucunu elde etmek için kullanılan "then" ve "catch" gibi fonksiyonlar yüksek seviye fonksiyonlardır.
Recursion: Örneğin, kendini tekrarlamalı olarak çalışan fonksiyonlar yüksek seviye fonksiyonlar olarak kullanılabilir.

# 14.Call Stack ,heap,stack,event loop,callback queue kavramlarını açıklayın.
- JavaScript'te, "call stack" (çağrı yığını) çalışan fonksiyonların veya işlemlerin yığınını ifade eder. JavaScript çalışırken, çalışan fonksiyonlar veya işlemler çağrı yığınına eklenir ve çalışması tamamlandığında çıkarılır. Bu, JavaScript'te çalışan işlemlerin geri izlenmesini ve hata ayıklama işlemlerini kolaylaştırırAynı zamanda, javascript'te recursion gibi yapılar kullanılırken çağrı yığını büyüyebilir. Recursive fonksiyonların her çağrısı çağrı yığınına eklenir ve işlem tamamlandığında çıkarılır. Bu nedenle, çok fazla recursion kullanımı çağrı yığını büyüdüğünden, "stack overflow" hatası oluşabilir.
Ayrıca, javascript'te "event loop" (etkinlik döngüsü) adı verilen bir mekanizma sayesinde, çağrı yığını büyümeden işlemlerin gerçekleştirilmesini sağlar. Bu mekanizma, işlemlerin gerçekleştirilmesini bekleyen işlemleri sıraya alır ve çağrı yığını boş olduğunda işlemleri gerçekleştirir. Bu sayede, çağrı yığını büyümeden uzun süreli veya yavaş işlemlerin gerçekleştirilmesi sağlanır.
Sonuç olarak, call stack Javascript'te çalışan fonksiyonlar veya işlemlerin geri izlenmesini ve hata ayıklama işlemlerini kolaylaştıran bir mekanizmadır. Ayrıca, recursion veya uzun süreli işlemlerin gerçekleştirilmesi için etkinlik döngüsü mekanizmasının kullanılması gerekir.
- Heap: JavaScript programlama dillerinde, "Heap" (yığın) bellekte dinamik olarak alınan ve serbest bırakılan verileri depolayan bir alandır. Heap, veri yapılarının oluşturulduğu ve yönetildiği bir alandır. Örneğin, nesneler, diziler veya fonksiyonlar gibi veri yapıları heap bellekte depolanır.
- Stack: JavaScript programlama dillerinde, "Stack" (yığın) fonksiyon çağrılarının veya işlemlerin gerçekleştirildiği yerdir. Stack, LIFO (Son Giren İlk Çıkar) yapısına sahiptir ve her çağrı veya işlem, stack'e eklenir ve tamamlandığında çıkarılır.
- Event Loop: JavaScript programlama dillerinde, "Event Loop" (etkinlik döngüsü) çağrı yığını (stack) büyümeden işlemlerin gerçekleştirilmesini sağlar. Event loop, işlemlerin gerçekleştirilmesini bekleyen işlemleri sıraya alır ve çağrı yığını boş olduğunda işlemleri gerçekleştirir.
- Callback Queue: JavaScript programlama dillerinde, "Callback Queue" (geri çağırma kuyruğu) işlemlerin gerçekleştirilmesini bekleyen geri çağırma fonksiyonlarının sıralandığı yerdir. Callback queue, event loop tarafından kontrol edilir ve çağrı yığını (stack) boş olduğunda geri çağırma fonksiyonları gerçekleştirilir.
# 15.Data fetching yöntemleri nelerdir.
JavaScript'te veri çekme yöntemleri arasında aşağıdakiler bulunur:
- XMLHttpRequest (XHR) : Eski bir veri çekme yöntemidir ve XmlHttpRequest nesnesi kullanılarak gerçekleştirilir. Bu nesne, tarayıcının arka ucunda veri çekmek için kullanılır ve AJAX istekleri gerçekleştirmek için kullanılır.
- Fetch API : Fetch API, XMLHttpRequest'in yerini alan modern bir veri çekme yöntemidir. Fetch API, JavaScript kodunuzda veri çekmek için kullanabileceğiniz bir dizi fonksiyon ve metodlar sunar.
- Axios : Axios, bir JavaScript kütüphanesidir ve Fetch API'nin yerini alan bir alternatif olarak kullanılabilir. Axios, daha kullanışlı ve kolay kullanılabilir bir arayüz sunar.
- jQuery : jQuery, JavaScript kütüphanesidir ve veri çekme işlemleri için kullanılabilir. jQuery, XMLHttpRequest veya Fetch API gibi alternatif yöntemlere göre daha kullanışlı ve kolay kullanılabilir bir arayüz sunar.
# 16.Bir fonksiyonu düzenli aralıklarla çalıştırmamızı sağlayan fonksiyonun adı nedir ? 
JavaScript'te bir fonksiyonu düzenli aralıklarla çalıştırmak için kullanabileceğiniz fonksiyon "setInterval()" dir. setInterval() fonksiyonu, belirtilen aralıkta belirtilen fonksiyonu tekrar tekrar çağırır. Örneğin, bir fonksiyonu her 5 saniyede bir çalıştırmak için setInterval() kullanabilirsiniz.

# 17. Bir fonksiyonu belirli bir gecikmeden sonra çalıştırmamızı sağlayan fonksiyonun adı nedir ?
JavaScript'te bir fonksiyonu belirli bir gecikmeden sonra çalıştırmak için kullanabileceğiniz fonksiyon "setTimeout()" dir. setTimeout() fonksiyonu, belirtilen zaman aralığı sonunda belirtilen fonksiyonu tek sefer çalıştırır. Örneğin, bir fonksiyonu 5 saniye sonra çalıştırmak için setTimeout() kullanabilirsiniz.
# 18.Constructor Nedir ? 
JavaScript'te, "constructor" (yapıcı) fonksiyonlar, nesnelerin oluşturulduğu ve özelliklerinin atandığı yerdir. Bir constructor fonksiyonu, bir nesne oluşturulduğunda çağrılır ve nesnenin özelliklerini ve davranışlarını tanımlar. Constructor fonksiyonları, class'lar veya prototype yapısı kullanılarak oluşturulduğunda kullanılır. 
Örneğin, bir "Person" sınıfı oluşturalım ve yapıcı fonksiyonunu kullanalım:
class Person { constructor(name, age) { this.name = name; this.age = age; } }
 const person1 = new Person("John", 30); 
console.log(person1.name); 
// "John" 
console.log(person1.age);
 // 30 
Bu örnekte, "Person" sınıfının yapıcı fonksiyonu, "name" ve "age" adlı iki özellik alır ve bunları nesnenin özellikleri olarak atar. Bu nesne oluşturulduğunda, yapıcı fonksiyon otomatik olarak çalışır ve nesnenin "name" ve "age" özellikleri atanır.

# 19. Call,apply,bind kavramlarını açıklayınız
- call()" metodu, bir fonksiyonu çağırmak için kullanılır ve ilk parametre olarak "this" değişkeninin değerini, diğer parametreler ise fonksiyonun gerçek parametrelerini alır.
- apply()" metodu, "call()" metoduna benzer şekilde çalışır ancak fonksiyon parametrelerini dizi olarak alır.
- bind()" metodu, bir fonksiyonu "this" değişkeninin değerini ve parametrelerini belirli bir değerle bağlamak için kullanılır. Bu metod, fonksiyonu çağırmaz ancak oluşan yeni fonksiyonu döndürür.
# 20.Babel nedir kullanmanın bize avantajları nelerdir ?
Babel, kodunuzu transpile ederken, JavaScript kodunuzu modern JavaScript özelliklerine dönüştürerek, tarayıcılar veya platformlar tarafından desteklenen daha eski JavaScript sürümlerine çevirebilir. Örneğin, ECMAScript 6 class'larını ve arrow functionlarını, ECMAScript 5'e dönüştürerek daha eski tarayıcılar veya platformlar tarafından desteklenen kod üretebilir. Ayrıca, Babel, kodunuzda kullandığınız özellikleri, desteklenmeyen tarayıcılar için polyfill (örnek kodlar) ile değiştirerek uyumlu hale getirebilir.




# 21.Dom ve Virtual DOM kavramlarını açıklayın
Document Object Model" (DOM), web sayfasının yapısını ve içeriğini programatik olarak değiştirmek için kullanılan bir API'dir. DOM, HTML veya XML belgelerini, bir ağaç yapısına dönüştürerek, belgenin elemanlarına veya özelliklerine programatik olarak erişmenizi sağlar. Örneğin, JavaScript kodunuzda bir HTML etiketine erişmek veya bir özellik değiştirmek için DOM kullanabilirsiniz.
"Virtual DOM" ise, JavaScript kodunuzda DOM'u yansıtmak için kullanılan bir veri yapısıdır. Virtual DOM, gerçek DOM'un yapısını ve içeriğini yansıtmak için kullanılır ve gerçek DOM ile senkronize edilir. Virtual DOM sayesinde, gerçek DOM'da yapılan değişiklikleri önceden simüle edebilir ve gerçek DOM'a yansıtmadan önce optimize edebilirsiniz.
# 22.prop ve component kavramlarını açıklayın
- "Prop" (properties), React komponentleri arasında veri aktarımını sağlamak için kullanılan bir kavramdır. Bir React komponentine veri aktarmanız için, o komponentin "prop" olarak tanımladığı değişkenlere değer atayabilirsiniz. Örneğin, bir "Ad" ve "Soyad" prop'larına sahip bir "Kullanıc" komponenti oluşturabilirsiniz ve bu prop'ları "Kullanıc" komponenti içinde kullanabilirsiniz.
- "Component" ise, React'te kullanılan bir kavramdır. React uygulamaları, birkaç düzeyde bileşenlerden oluşur. Her bileşen, bir parçası oluşturduğu daha büyük bir bileşenin içeriğidir. React bileşenleri, HTML veya JSX kodu içerebilir ve veri işleme, birleştirme veya görüntüleme işlemlerini gerçekleştirebilir. React bileşenleri, fonksiyonel veya sınıf tabanlı olabilir. Bir React bileşeni, kendi içinde diğer bileşenleri içerebilir veya diğer bileşenler tarafından çağrılabilir. Bu yapı sayesinde, uygulamanızı daha küçük parçalara bölerek, okunaklı ve maintainable yapabilirsiniz.
React bileşenleri, props ve state değişkenleri aracılığıyla veri alabilir ve bu verileri içeriğinde kullanabilir. Props, bileşenin dışarıdan veri almasını sağlar ve değiştirilemez. State ise bileşenin kendi içinde tuttuğu değişkenlerdir ve bileşenin içeriğini etkileyebilir. State değişkenleri bileşen tarafından yönetilir ve bileşen içinde değiştirilebilir.
# 23.React Prop Drilling nedir ?
"Prop drilling" (prop tunneling), React uygulamalarında veri aktarımı için kullanılan bir kavramdır. Bu terim, verinin uygulamanın farklı katmanları arasında geçerek, tüm bileşenler arasında verinin prop olarak aktarılmasını ifade eder. Örneğin, bir verinin uygulamanın en üst seviyesinde oluşturulduğu ve tüm alt seviyedeki bileşenlere prop olarak aktarılmasını ifade eder.
Bu yapı, verinin uygulamanın farklı katmanları arasında geçerek, tüm bileşenler arasında verinin prop olarak aktarılmasını ifade eder. Bu yapı, verinin uygulamanın en üst seviyesinde oluşturulduğu ve tüm alt seviyedeki bileşenlere prop olarak aktarılmasını ifade eder. Bu yapı sayesinde, bileşenler arasındaki veri aktarımı kolaylaşır ancak bileşenler arasındaki ilişki karmakarışık olabilir, yönetimi zorlaşır ve performans sorunlarına yol açabilir.
Bu yüzden, veri aktarımı için alternatif yöntemler önerilmektedir. Örneğin, context API veya Redux gibi veri yönetim kütüphanelerini kullanmak, veri aktarımını daha kontrollü ve okunaklı hale getirebilir.


# 24.Neden Hooklar component’in en yukarısında çağırılır.
React Hooks, fonksiyonel bileşenlerde state yönetimi veya lifecycle metodlarının kullanımını sağlar. Hooks, fonksiyonel bileşenlerde kullanıldığında, componentin en yukarısında çağrılması gerekir.
Bu, React'in bileşenin ne zaman re-render edileceğini belirlemek için kullandığı bileşen içeriğinin değişip değişmediğini anlamasına yardımcı olur. Hooklar, bileşenin her render edildiğinde çağrılır ve bu, state veya props değişkenlerinin değiştiğinde bileşenin yeniden render edilmesini sağlar.
Eğer Hookler componentin içinde yer alırsa, React hangi Hook'un ne zaman çalıştırılması gerektiğini belirleyemez ve bu da hata oluşmasına neden olabilir. Ayrıca, Hookların componentin en yukarısında çağrılması sayesinde, kodun okunaklılığı ve anlaşılırlığı arttırılmış olur.

# 25. Class component ve functional component arasındaki farklar nelerdir ?
React bileşenleri, fonksiyonel veya sınıf tabanlı olarak yazılabilir. Bu iki yöntem arasındaki farklar şunlardır:
Fonksiyonel bileşenler: Fonksiyonel bileşenler, JavaScript fonksiyonları olarak yazılır ve props veya state değişkenlerini alabilirler. Fonksiyonel bileşenler, state yönetimi için useState() veya lifecycle metodları için useEffect() gibi React Hooks kullanabilirler. Fonksiyonel bileşenler, performans açısından daha avantajlıdır ve daha kolay okunur ve anlaşılır.
Sınıf bileşenler: Sınıf bileşenler, ES6 sınıfları olarak yazılır ve this anahtar kelimesi ile state ve lifecycle metodlarına erişebilirler. Sınıf bileşenler, performans açısından daha yavaş olabilir ve daha karmakarışık olabilir.
Sonuç olarak, iki yöntem arasında performans açısından fonksiyonal componentlar daha iyidir ancak sınıf tabanlı componentlar daha tanıdık olabileceğinden, yazarların tercihine göre her ikiside kullanılabilir.

# 26.React Lifecylce metodları nelerdir.
React bileşenleri, bileşenin oluşturulduğu, güncellendiği veya silindiği zaman çağrılabilen lifecycle metodlarına sahiptir. Bu metodlar aracılığıyla bileşenin içeriği veya props/state değişkenleri güncellenebilir.React bileşenlerinin lifecycle metodları şunlardır:
- componentDidMount(): Bileşen oluşturulduğu ve ilk kez DOM'a eklendiği zaman çağrılır. Bu metod, bileşenin ilk görüntülenmesi için gerekli olan veri veya işlemleri yapmak için kullanılabilir.
- componentDidUpdate(): Bileşenin props veya state değişkenleri güncellendiği zaman çağrılır. Bu metod, bileşenin güncellenen verilerle yeniden render edilmesi için gerekli olan işlemleri yapmak için kullanılabilir.
- componentWillUnmount(): Bileşen DOM'dan silindiği zaman çağrılır. Bu metod, bileşenin silinmesi sonrası gerekli olan işlemleri yapmak için kullanılabilir.
- shouldComponentUpdate(): Bileşenin props veya state değişkenleri güncellendiği zaman çağrılır. Bu metod, bileşenin render edilip edilmeyeceğini belirlemek için kullanılabilir.
- getDerivedStateFromProps(): Bileşenin props değişkenleri güncellendiği zaman çağrılır. Bu metod, bileşenin state değişkenlerini güncellemek için kullanılabilir.
Lifecycle metodları, sadece sınıf tabanlı componentlerde kullanılabilir.




# 27.Syntetic Events Nedir ?
Synthetic Events, React bileşenlerinde DOM etkileşimleri için kullanılan bir event sistemidir. Synthetic Events, aslında JavaScript tarafından yönetilen ve DOM eventleri ile aynı davranış gösteren, JavaScript tarafından oluşturulan eventlerdir.
Bu sayede React bileşenleri, DOM eventleri ile aynı şekilde çalışır ve sadece JavaScript tarafından yönetilir. Bu sayede React, bileşenler arasındaki etkileşimleri ve eventleri daha kontrollü ve anlaşılır hale getirir. Aynı zamanda, Synthetic events ile browser farklılıklarının oluşmamasını ve kodun daha kolay test edilmesini sağlar.

# 28. Build almak ne anlama gelir, build işlemi esnasında neler olur.
"Build" işlemi, bir yazılım projesinin üretim veya dağıtım için hazır hale getirilmesi anlamına gelir. Bu işlem, kaynak kodların derlenmesi, bağımlılıkların eklenmesi, dosya boyutlarının azaltılması ve diğer işlemlerin gerçekleştirilmesi olarak tanımlanabilir.
- Build işlemi esnasında genellikle şunlar gerçekleşir:
- Kaynak kodlar derlenir, transpile edilir ve minify edilir
- Bağımlılıklar yönetilir, gerekli paketler yüklenir ve projede kullanılan bağımlılıkların güncellenmesi sağlanır.
- Dosya boyutları azaltılır, gereksiz dosyalar silinir ve dosya adları optimize edilir
- Proje ayarları ve config dosyaları kontrol edilir ve güncellenir
- Testler çalıştırılır ve sonuçlar rapor edilir
- Proje üretim veya test ortamına deploy edilir.
Bu işlemlerin amacı, projeyi üretim veya dağıtım için hazır hale getirmektir. Bu sayede projede oluşan hatalar veya sorunlar önceden tespit edilir ve çözülür. Aynı zamanda proje daha hızlı ve daha az kaynak tüketen hale getirilir.

# 29.Webpack Nedir ?
Webpack, JavaScript modül yükleyicisi ve paketleyicisidir. Bu araç, JavaScript, CSS, resim gibi dosyalarınızı modüller halinde tarayarak, bunları tek bir veya birden fazla dosyaya paketler. Bu sayede, tarayarak bulunan modülleri ve bağımlılıkları bir araya getirerek projenizin performansını arttırır.
Webpack, sadece JavaScript dosyalarını değil aynı zamanda HTML, CSS gibi diğer dosya türlerini de işleyebilir. Webpack ile, sadece projede kullanılan modülleri ve bağımlılıkları yükler, böylece proje hızlı ve küçük olur. Ayrıca Webpack ile, sadece tarayıcılar için çalışan kodları üreterek, eski tarayıcılar için gereksiz kodları üretmezsiniz.






 # 30. React memo,usememo,usecallback hooklarını açıklayınız.
React, performansı arttırmak için bazı Hook'lar sunar. Bunlar:
React.memo: Bu Hook, fonksiyonel bileşenlerin tekrar render edilmemesini sağlar. React.memo kullanarak, bileşenin props değişmeden önce render edilip edilmeyeceğini kontrol eder. Props değişmediyse, bileşen tekrar render edilmez. Bu sayede, uygulamanın performansı arttırılır.
useMemo: Bu Hook, belirli bir değerin değişmeden önce hesaplanıp hesaplanmayacağını kontrol eder. Eğer değer değişmediyse, önceki değer kullanılır. Bu sayede, performansı arttırmak için hesaplamaların tekrar yapılması engellenir.
useCallback: Bu Hook, belirli bir fonksiyonun değişmeden önce oluşturulup oluşturulmayacağını kontrol eder. Eğer fonksiyon veya fonksiyonun bağımlılıkları değişmediyse, önceki fonksiyon kullanılır. Bu sayede, performansı arttırmak için fonksiyonların tekrar oluşturulması engellenir.
Bu Hooklar sayesinde, React bileşenlerinin performansı arttırılır ve bileşenlerin yanıltıcı bir şekilde re-render edilmesi engellenir. Bu sayede, uygulamanın hızı ve verimliliği arttırılır.

# 31.State Menagement yöntemleri nelerdir ?
React uygulamalarında state yönetimi, uygulamanın veri durumunun nasıl tutulacağını ve nasıl yönetileceğini belirler. State management yöntemleri arasında en yaygın olanlar şunlardır:
- Local state: Her bileşenin kendi içinde yer alan state'i yönetir. Bu yöntem, uygulamanın küçük ve basit olması durumunda kullanılabilir. Ancak, uygulama büyüdükçe, state yönetimi zorlaşabilir.
- Context API: React'in kendi içinde yer alan bir yöntemdir. Bu yöntem, state'i kapsayan bir context oluşturulur ve bileşenler bu context'e bağlanır. Bu sayede, state'i yönetmek isteyen bileşenler context'e erişebilir. Bu yöntem, uygulama boyutu büyüdükçe daha pratik hale gelir.
- Redux: React uygulamaları için popüler bir state management kütüphanesidir. Bu kütüphane, state'i tek bir noktada (store) yönetir ve bileşenler bu store'a erişir. Bu yöntem, uygulamanın büyüklüğünden bağımsız olarak kullanılabilir. Ancak, kurulumu ve kullanımı biraz daha zahmetli olabilir.
- MobX: MobX, Redux ile benzer bir şekilde çalışır. Bu kütüphane de state'i tek bir noktada yönetir ve bileşenler bu state'e erişir. MobX, Redux'a göre daha az kurulum gerektirir ve kullanımı daha kolaydır.
Bu yöntemler arasında kullanılacak olanı, uygulamanın boyutu, ihtiyaçları ve geliştiricinin tercihi gibi faktörlere göre seçilir.

# 32.Context API ve Redux Nedir,Farkları Nelerdir ?
- Context API: React'in kendi içinde yer alan bir yöntemdir. Bu yöntem, state'i kapsayan bir context oluşturulur ve bileşenler bu context'e bağlanır. Bu sayede, state'i yönetmek isteyen bileşenler context'e erişebilir. Bu yöntem, uygulama boyutu büyüdükçe daha pratik hale gelir.
- Redux: React uygulamaları için popüler bir state management kütüphanesidir. Bu kütüphane, state'i tek bir noktada (store) yönetir ve bileşenler bu store'a erişir. Redux, state'i tek bir yerde yönetir ve bileşenlerin state'e erişimini kontrol eder. Ayrıca, state'in geçmişini kaydetme ve geri dönme özellikleri de sağlar.
Context API, Redux'a göre daha az kurulum gerektirir ve kullanımı daha kolaydır. Ancak Redux daha esnek ve scalabilirdir ve kodun anlaşılmasını ve debuggability'i kolaylaştırır. Redux, özellikle uygulamanın büyüklüğü ve karmaşıklığı arttıkça daha yararlı olabilir.




# 33. SSR,CSR,SSG kavramlarını açıklayın ?

- SSR (Server-Side Rendering): Bu yöntem, uygulamanın sunucuda render edilmesini sağlar. Bu sayede, tarayıcıda uygulama ilk yüklendiğinde hızlı bir şekilde gösterilir. SSR, SEO'yu arttırmak ve tarayıcıda ilk yüklenmenin hızını arttırmak için kullanılır.
- CSR (Client-Side Rendering): Bu yöntem, uygulamanın tarayıcıda render edilmesini sağlar. Bu sayede, tarayıcıda uygulama ilk yüklendiğinde yavaş bir şekilde gösterilir. Ancak, daha sonra uygulamanın hızı arttır.
- SSG (Static Site Generation): Bu yöntem uygulamanın statik olarak üretilmesini sağlar. Bu sayede, uygulamanın hızı arttırılır ve SEO'yu arttırmak için kullanılır. Bu yöntem, özellikle blog veya haber siteleri gibi statik içerikli siteler için idealdir.
Bu kavramlar arasında farkları, uygulamanın nasıl yüklenir ve nasıl gösterilir. SSR ile sunucuda render edilir ve hızlı yüklenir, ancak daha büyük sunucu ihtiyacı vardır. CSR ise tarayıcıda render edilir ve daha sonra hızlı yüklenir, ancak ilk yükleme yavaş olabilir. SSG ise statik olarak üretilir ve hızlı yüklenir, ancak sadece statik içerikli siteler için kullanılabilir.








