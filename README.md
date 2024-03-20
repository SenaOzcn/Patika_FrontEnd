# Patika.dev Frontend Web Patikası Eğitiminden Notlar

## Emmet’deki Kısa Yollar

<ol>
  <li> > ifadesini kullanarak kardeş element oluşturuyoruz.<p>Örneğin şekildeki, gibi ul tagı içerisinde li tagı oluşturmak istiyorsunuz. Bunun için yapmanız gereken tek şey <b>ul>li</b> yazarak Tab’a basmak.</p>
    
         
        <ul>
          <li></li>
        </ul>  

   <p>Bu işlemi yaptıktan sonra ul tagına eklemek istediğimiz bir kardeş eleman kalmayınca ise <b>^</b> ifadesini kullanarak ul tagı dışına çıkıp yeni taglar oluşturabiliriz.</p>

   <p>Örneğin ul tagı içinde li tagı oluşturduktan sonra ul tagı dışında bir p tagı eklemek istiyorum. Bunun için <b>ul>li^p</b> yazarak taba basabilirim.</p>
  
        <ul>
          <li></li>
        </ul>
        <p></p>

  </li>
  <li>
    Peki ya bu ul tagı içerisine birden fazla li oluşturmak istiyorsam, ne yapmalıyım?

   <p>Bunun için * ifadesini kullanırız. <b>ul>li*3</b> yaparak ul tagı içerisinde üç adet li tagı oluşturabilirsiniz.</p>

        <ul>
          <li></li>
          <li></li>
          <li></li>
        </ul>
   
  </li>
  <li>
    Bunu yerine benzer biçimde kardeş eleman-tag eklemek için + ifadesi de kullanılabilirdi: <b>ul>li+li+li</b>
  </li>
  <li>
    Tag eklerken onlara <i>class</i> özelliği vermek için de <b>.</b> ifadesini kullanırız.
    <p>Örneğin ul.class1>li.class2 yazılarak tab tuşuna basıldığında:</p>

        <ul class="class1">
          <li class="class2"></li>
        </ul>

 <p>Bu şekilde bir kod oluşur.</p>
    <p>Aynı şekilde <b>ul.class1>li.class2*3</b> denerek bir yerine üç adet class2 sınıfından li tagı oluşturulabilirdi.</p>

        <ul class="class1">
          <li class="class2">
          <li class="class2">
          <li class="class2">
        </ul>
    
  </li>
  <li>
    Bir id özelliği eklemek için ise <b>#</b> ifadesini kullanırız. 
    <p>Yeni bir örnekle id özelliği eklemeyi görelim. <b>ul#id1>li#id2</b> diyerek aşağıda gördüğünüz kodu oluşturabiliriz.</p>

        <ul id="id1">
          <li id="id2></li>
        </ul>

  </li>
  <li>
    Burada <b>+</b> ve <b>*</b> ifadesinin farkını da daha kolay anlayabiliriz.
    <p>Örneğin ul tagının içine <b><i>aynı</i></b> id’ye sahip 3 adet li eklemek istiyorsam * ifadesi kullanılabilir. <b>ul>li#id*3</b></p>

        <ul>
          <li id="id">
          <li id="id">
          <li id="id">
        </ul>
    
  <p>Fakat amacım <b><i>farklı</i></b> id’lere sahip üç adet li tagı oluşturmaksa <b>ul>li#id1+li#id2+id#id3</b> yapılır.</p>

        <ul>
          <li id="id1"></li>
          <li id="id2"></li>
          <li id="id3"></li>
        </ul>
  
  </li>
  <li>
    Peki otomatik artış sağlayan değerleri tek tek yazmak amacımız zaman tasarrufu iken ne kadar mantıklı?
    <p>Emmet bunun için de bir kısa yola sahip: <b>$</b> ifadesi. Yani yukarda görmüş olduğunuz <b>ul>li#id1+li#id2+li#id3</b> şeklinde yazdığımız kod bloğunu çok daha basit bir biçimde <b>ul>li#idNo$*3</b> diyerek yazabiliriz.</p>
<p>Böylece otomatik olarak idNo1, idNo2 ve idNo3 idlerine sahip üç adet li tagımız olur.</p>

        <ul>
          <li id="idNo1"></li>
          <li id="idNo2"></li>
          <li id="idNo3"></li>
        </ul>
    
  </li>
  <li>
    Sırada oluşturulan tagların içine text yazılması var:
    <p>Textlerimizi <b>{}</b> ifadesinin içine yazmamız yeterli: <b>p{Emmet ile tag içine text yazma}</b></p>

        <p>Emmet ile tag içine text yazma</p>
    
  </li>
  <li>
    Bir diğer emmet kısa yolunu ise kodumuzda içerik olmadığı zamanlarda kullandığımız anlamsız yazıları yani "<b>lorem ipsum</b>"ları oluşturmak için kullanıyoruz.
    <p>Örneğin bir paragraf oluşturacaksınız ve bu paragrafın henüz bi içeriği yok fakat boş durmasındansa oraya metin geleceğini belirtmek istiyorsunuz veya metin geldiğinde nasıl görüneceğini görmek istiyorsunuz. Anlamsız harfler veya zaman gerektiren rastgele cümleler oluşturmak yerine bu kısayolu kullanabilirsiniz : <b>p>lorem</b> Taba bastığınızda aşağıdaki gibi bir çıktı alacaksınız.</p>

        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Totam consequatur ipsa quos vero voluptas incidunt molestias autem dicta sit, minus alias inventore in nemo. Laboriosam accusamus nobis sunt nesciunt ducimus?</p>

    
  </li>
  <li>
    Bu kadar uzun bir lorem yazısı istemiyorsanız yapmanız gereken tek şey lorem yazdıktan sonra yanına kaç kelimeli bir lorem oluşturmak istediğinizi eklemek.
    <p>Örneğin <b>5 kelimeli bir lorem yazısı</b> istiyorsunuz. Bunun için <b>p>lorem5</b> yazmanız yeterli.</p>

        <p>Lorem ipsum dolor sit amet.</p>
    
  </li>
  <li>
    Son olarak Emmet’in bir özelliğinden bahsedeceğim. <b>li.className</b> yazıp Tab’a bastığımızda ne oluşmasını bekleriz? Evet className class’ına ait bir li tagı oluşmasını. Peki herhangi bir tag koymaksızın sadece <b>.className</b> yazdıktan sonra Tab’a basarsak ne olur?
<p>Cevap:</p>

        <div class="className"></div>

<p>Gördüğünüz gibi bir div oluşturdu. Emmet’e bir tag vermeksizin . veya # ifadelerini kullandığımızda bunun <b><i>div</i></b> tagı olduğunu biliyor.</p>
<p>Ama biz bunu <b>ul</b> tagı içinde denersek tepkisi ne olur? Hadi deneyelim!:</p>
    
        <ul>
            <li class="className"></li>
        </ul>

<p>Gördüğünüz gibi <b>ul>.className</b> yazıp Tab’a bastığımızda ise bunun li elementi olduğunu algılıyor.</p>
<p>Emmet’in kendi sitesindeki cheat sheete <a href="https://docs.emmet.io/cheat-sheet/">buradan</a> ulaşabilirsiniz.</p>
  </li>
</ol>
