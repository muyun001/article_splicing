所有文件：
    1.n个文件夹,如“光电传感器”文件夹等，每个文件夹下目录结构（以光电传感器为例）：
        光电传感器：
                    - img ：存放图片
                    - 光电传感器首段.txt       里面有 m 段文字
                    - 光电传感器中段.txt       里面有 n 段文字
                    - 光电传感器尾段.txt       里面有 k 段文字

    2.keyword.xlsx ： 存放所有关键词


任务：
    1.在keyword.xlsx表格中随机抽出一个关键词，备用；
    2.在同目录的img文件夹下随机抽出两张图片，备用；
    3.分别在m和k段文字中各任意抽出一段，在n段文字中任意抽出三段，将这五段文字组成一篇文章。
        要求：
            1)原首段中的文字还是在首段，中段在中段，尾段在尾段；
            2)每段文字左右两侧添加<p>标签，如：
                <p>除了结构上的不同，反射型光电传感器的检测方法也很突出，而且灵敏度也很高。这么多特点若是大家都不知道，那真是非常可惜的，所以一定要认真记哟。</p>
    4.将1中的关键词作为标题，插入文章中的第一行。
        要求：标题左右两侧添加<h1>标签，如：
            <h1>广东低价的光电传感器批发价</h1>
    5.将1中的关键词分别插入2中文章的首段和尾段。
        要求：
            1)关键词随机插入在逗号或者句号的右侧；
            2)每篇文章插入关键词的次数在2~3次。
    6.将2中的图片分别插入文章的第二段和第四段下方。
        要求：格式如下：
            <p><img src={imgpath}/image/防尘槽型光电开关/tu6.png></p>
            (图片是“image/防尘槽型光电开关”文件夹下的tu6.png)
    7.以“关键词.txt”命名，将文章输出。

    注:有多少个关键词即输出多少篇文章。



大体实现流程：
    1.创建all_article_list，存放所有文件夹下生成的所有的文章列表；
    2.先对每个文件夹进行操作;
        1)对中段文字随机抽出的三段进行排列组合，看一共有多少种抽取结果，形成一个listB列表，listB中的每个元素还是个list，此list中存放抽取的三段文字；
        2)首段和尾段的所有段落，分别形成listA，listC；
        3)对listA，listB，listC 进行排列组合，生成一个article_list，其中存放所有可能生成的文章列表
        4)将article_list中的数据存放到all_article_list中。
    3.重复执行2流程，直到把所有文件夹下生成的文章都放到all_article_list中。
    4.在all_article_list中随机抽取一篇文章，在keyword.xlsx中随机抽取一个关键词，将此关键词插入到此文章的首段和尾段；
    5.在第二段和第四段后面插入“img”图片下的任意两张图片；
    6.文章输出。



最终生成文章举例：

<h1>广东低价的光电传感器批发价</h1>
<p>你必须要知晓的反射型光电传感器。广东低价的光电传感器批发价光电传感器，一种被广泛应用于机械和实验和器具，可能很多人会对它感到陌生，但在实际上，我们的日常生活也是离不开这个神奇的光电传感器的，那么作为其非常重要的一种类型，不知道大家有没有听说过反射型光电传感器。我们日常的验钞机和复印机就是应用的这种原件，下面就来随小编一起来了解一下反射型光电传感器吧</p>
<p>反射型光电传感器的简单介绍反射型光电传感器，顾名思义就是一种依靠反射来进行运作的光电传感器，它的工作原理就是通过把光的强度的变化转换成电信号的变化来实现检测的。它一般由发射器、接收器和电路组成，由发射器向被检测物体发出光束，再由接收器接收被检测物体所反射的光线，并将收到的光的信号转化为带有电的信号，从而完成任务，它的工作过程看起来简单，实际上是非常复杂的。
</p>
<p><img src={imgpath}/image/防尘槽型光电开关/tu2.png></p>
<p>除了结构上的不同，反射型光电传感器的检测方法也很突出，它的检测反应比较快，解析度也高，测量精度准，而且灵敏度也很高。因为它的制作材料不含铅，还容易散热，所以使用寿命也比较长，不得不说是一种新的绿色环保能源。还有因为它的结构简单，所以它的形式变化也很灵活。这么多特点若是大家都不知道，那真是非常可惜的，所以一定要认真记哟。
</p>
<p>反射型光电传感器的应用，在一开始就已经提到了，反射型光电传感器的应用范围较小，这个范围说的是它应用的领域，它的应用几乎都是在民用领域，比如说鼠标，鼠标的反应靠的就是反射型光电传感器，往大了说，打印机在扫描的时候也是应用了反射型光电传感器，其他的像是扫描仪、感应洁具也是应用了它。在上述提到的产品里，没有那个是真正足够大的吧，这下子跟上文都可以对上号了吧，大家也放心了吧。如果大家在生活中再多一些认真，那么如果是自己发现反射型光电传感器的优点的话，肯定比我告诉大家的感觉要好上不止一倍。
</p>
<p><img src={imgpath}/image/防尘槽型光电开关/tu6.png></p>
<p>以上就是对反射型光电传感器的介绍了，相信大家在看完以后已经对反射型光电传感器有了更深的了解了吧。反射型光电传感器，虽然听起来很陌生，但是在点钞机、限位开关、计数器、电机测速、打印机、复印机和计数等领域都有广泛的应用，广东低价的光电传感器批发价为我们的生活提供了诸多的便利，真心希望通过以上文字能让大家熟悉反射型光电传感器。
</p>
