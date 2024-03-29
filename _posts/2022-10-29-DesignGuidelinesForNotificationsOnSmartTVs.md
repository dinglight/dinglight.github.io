# 智能电视中的通知设计指南
(DesignGuidelinesForNotificationsOnSmartTVs)

# 摘要
通知是许多智能设备的核心机制之一。智能手机、智能手表、平板电脑和智能眼镜都提供了类似的方法来通知用户。但是，对于智能电视，目前还没有建立标准的通知机制。智能电视和其他智能设备不同，因为智能电视通常被多个用户同时使用。我们不清楚智能电视上的通知应该如何设计，我们也不知道用户需要哪些信息。从一组焦点小组中，我们得到了智能电视上通知的设计空间。我们通过在在线调查和实验室研究中进一步研究选定的设计方案，例如，当用户与他人一起看电视时，他们需要不同的信息，隐私是一个主要问题。我们根据智能电视上的通知的设计指南，开发人员可以用有意义的方式来获得用户的注意力。

# 关键词
通知，智能电视，指南，信息接口和展示

# 介绍
今天的移动设备和传统的台式电脑通过通知来告知用户新消息、即将到来的约会、事件和一般提示。通知是一种完善的机制，用于告知用户各种各样的信息。一个主要用例是启用异步通信。在所有主要平台上，一个典型的与个人通信相关的通知内容就是告知用户发件人是谁并显示文本摘录。近年来，通知成为许多智能设备的核心机制之一。

通知可以提供时间敏感的信息。然而，它们并不总是及时到达用户，因为设备不在用户的范围内。例如，Dey等人的研究[6]显示，用户的智能手机只有在53%的情况下在用户的身边。早在2002年，Want等人[23]就提议在不同的智能设备之间分发通知。Sahami等人[21,24]开发了一种将智能手机通知转发到台式电脑的系统。最近，各大智能手机平台开始提供集中通知机制。通知不仅在单个设备上管理，而且在智能手机、平板电脑、台式电脑和笔记本电脑之间收集和共享。此外，最近出现了许多新型智能设备。智能手表和智能眼镜的核心功能是显示通知。然而，Lyons[16]在研究智能手表用户时发现，50名参与者中有24%的人在家不戴手表。

另一种非常成功的智能设备类型是智能电视。与普通电视相比，智能电视的主要特点是能够处理数据和连接在线服务。因此，从互联网上播放视频和其他内容成为可能。与移动操作系统不同的是，目前还没有占据主导地位的电视操作系统。然而，一个明显的趋势是类似于移动操作系统的平台，包括通过从应用商店安装应用程序来扩展系统的可能性。与其他智能设备相比，目前的智能电视还没有建立通知机制。在智能电视上显示通知带来了许多挑战。电视主要用于观看内容，包括电视剧、新闻和电影。在主要内容的上方显示通知会导致分心，从而影响电视体验。此外，与智能手机或智能手表不同的是，电视是供多人同时使用的共享设备。因此，针对其他智能设备设计的通知机制不能直接用于智能电视。相反，它必须研究如何在所有设备上实现愉快的通知体验，同时尊重用户的注意力和隐私。

在本文中，我们制定了智能电视上的通知的设计指南。本文的结构如下:通过一系列焦点小组，我们首先探索潜在用户设想的设计方案。通过这个设计空间，我们进一步研究了五种不同的在线调查设计方案。基于研究结果，我们开发了一个可定制的智能电视应用程序，它能够在看电视时显示通知，我们用它来进行实验室研究。结合焦点小组、在线调查和实验室研究的结果，我们得出了智能电视上通知的设计指南。这些设计指南可以被未来电视系统的开发人员使用，以一种有意义的方式获得用户的注意力。

# 相关工作
智能设备的主要特征是能够连接到其他智能设备和互联网。在过去的几年里，现有的设备和日常用品变得更加智能。有了移动数据网络，人们可以随时上网，而有了智能手机，它可以放在口袋里。智能手表和智能眼镜扩展了智能手机，并始终与用户在一起。智能电视能够从网络传输内容，从而将电视从一个主要用于看电视的设备转变为一个能够从各种来源接收内容的大屏幕。智能设备的连接性允许将消息推送到设备，这为通知奠定了基础。当收到推送信息时，智能设备可以通过多种方式提醒用户，即视觉提示、听觉信号和触觉输出。

在智能手机上，通知是一种核心的交互机制。大多数当前的移动操作系统允许从任何屏幕上通过一个简单的手势访问待处理通知列表。之前的工作研究了通知在台式电脑、智能手机和智能手表上的影响。在一项有15名参与者的原位研究中，Pielot等人调查了用户如何与通知交互。在一周的时间里，参与者平均每天收到63.5条通知，大部分来自即时消息和电子邮件应用程序[19]。此外，该研究表明，通知会在几分钟内被查看到，即使是在智能手机被设置为静音模式的情况下。Sahami等人通过收集4万名用户[21]的2亿条手机通知，对智能手机通知进行了大规模分析。他们发现，用户会及时查看通知，有50%的通知会在30秒内被查看。分析结果显示，与消息传递、通信和日历事件相关的通知是用户最看重的。此外，作者得出结论，重要的通知是关于人和事件的。

关于通知引起的中断的研究早于当前智能设备的出现。Czerwinski等人研究了中断对传统桌面pc[5]任务切换的影响。根据Iqbal等人的研究，通知虽然会造成干扰，但仍然受到用户的重视，因为它们提供了认知[12]。研究表明，通过定时通知可以减少通知的破坏性影响。通过在任务结束时发出通知，可以保持高认知并减少通知[1]的破坏性影响。Fallman和Yttergren提出了一种手机系统，可以检测到附近的用户，并相应地选择合适的通知方式。

如今，人们经常同时使用多种设备。例如，智能手机正成为电视的第二个屏幕，通过社交网络[15]提供交互功能。Nathan等人实现了CollaboraTV，一个异步交互系统，目标是将人们聚集在一起，即使他们不在同一时间或地点观看[17]。为期一个月的实地研究结果显示，参与者对该系统很重视。Alaoui和Lewkowicz提出了一个类似的老年人应对孤独的系统[2]。

霍尔兹等人[11]在一项研究中发现，家庭成员在客厅里聚集在一起，进行身体上的交流。库尔图瓦[4]发现有三种看电视的行为。第一种只关注电视，第二种用第二屏幕看电视，比如平板电脑或笔记本电脑，第三种使用第二屏幕甚至印刷媒体。

在电视节目推荐系统领域已经做了进一步的工作。Chang等人给出了文献综述，并基于获得的见解，提出了一个推荐框架[3]。由于推荐是基于用户的兴趣，这给多个用户带来了挑战。解决这些挑战的一个可能的办法是合并电视机前的人的兴趣资料，就像Shin和Woo[22]所提出的那样。Lee等人提出了一个智能电视系统，可以使用人脸识别[14]对用户进行身份验证。这可以用于根据电视机前的用户自动更改节目推荐。此外，研究人员提出利用手部检测技术，以自然手势控制智能电视。

Regan和Todd[20]探索了一个系统，允许多个用户在看电视的同时访问他们的即时消息。他们指出，除了看电视外，人们还经常使用个人电脑进行交流。他们研究了与多人在同一房间看电视时，这种系统对隐私和注意力分散的影响。为了让用户意识到收到的消息，他们在屏幕的角落使用了弹出提醒，类似于在PC上发现的提醒。在一项研究中，他们发现对一些人来说，即使在看电视的时候，使用即时通讯工具也是很重要的。在这项研究中，如果收到的信息不是发给参与者的，就会被认为是打断了。

Hess等人对社交电视体验的概念[10]进行了实证研究。他们表示，通过目前的技术，网络和电视相结合，使用户能够分享内容，并与他人进行远程交流。他们发现了一种趋势，即看电视被其他媒体所补充。同时使用多个设备，例如与朋友交流。在一个研讨会上，一个小组讨论通知。信息应该在智能手机上接收，但用户应该能够决定通知是应该显示在智能手机上，电视上，还是两者都显示。Neate等人[18]调查了在看电视时如何将注意力吸引到第二个屏幕上的相关内容。他们执行了一些刺激，包括一个显示在电视角落的图标。在Geerts等人进行的一项研究中，“请勿打扰”模式被证明为必要的[8]。然而，研究人员提到，用户并不希望每次他们不想被打扰时就启用或禁用这种模式。

综上所述，通知是当前智能设备的核心功能。它们用于通过多种方式向用户发出警报。虽然有大量研究智能电视使用的工作，但还没有建立智能电视的标准通知机制。缺少的是智能电视上通知的设计指导方针。

# 焦点小组
我们组织了三个焦点小组来探索智能电视上通知的设计空间。每个焦点小组持续约一个小时，在一个配有白板和投影仪的会议室举行。我们提供了便利贴和黑色白板笔、磁铁和毡头笔(三种不同颜色)，以及印着电视的A4纸。在焦点小组期间，我们提供了零食和饮料。我们为参与者的时间补偿了10欧元。在所有小组中，一名研究人员指导讨论，另一名研究人员做笔记并写下参与者的陈述。在下面我们首先描述以Goodman等人为基础的焦点小组的程序[9]。之后，我们提供了关于参与者和他们在智能电视方面的行为的信息。然后我们展示结果，然后是总结和讨论。

## 步骤
每个焦点小组都有相同的结构，包括四个部分:介绍、创意、开放讨论和最后的总结讨论。

### 介绍
首先，向与会者简要介绍了焦点小组的主题。我们准备了幻灯片，解释了各种智能设备上的通知的当前状态，智能电视上的通知的缺失，以及我们想如何探索它们。此外，我们鼓励与会者在会议期间自由发言，要求避免在同一时间讲话。之后，我们请他们自我介绍。在介绍环节中，所有参与者首先说出自己的名字，并告诉小组成员自己拥有的能够通知自己的设备类型，以及他们能想到的最后一个重要通知。此外，参与者陈述了他们是否拥有电视，并简要谈论了他们看电视的行为。

### 创意
在介绍环节结束后，我们要求参与者想象一台可以通知他们事件的电视，比如短信、电子邮件或日历提醒。我们分发了几张印着电视的纸，让参与者勾画出这样一个系统应该是什么样子以及它应该如何运行。我们要求他们考虑多个因素，包括通知的内容、大小、位置和显示时长。大约10分钟后，我们要求参与者与旁边的人讨论他们的想法。我们指导他们谈论他们的想法的积极和消极方面，并选出他们最喜欢的想法。

### 开放讨论
创意完成后，我们将参与者挑选的所有草图收集起来，钉在白板上。图1显示了讨论阶段的一个焦点小组。我们要求参与者向小组其他成员解释他们的创意。随后，我们询问了小组其他成员对这个创意的看法，包括优点和缺点。如果没有任何参与者提出意见，我们就会问他们，他们的创意在他们独自看电视和和别人一起看电视时是分别如何工作的。

### 结束讨论和总结
在讨论了所有参与者的想法后，我们与团队探讨了在电视上的通知可以走多远。我们询问了他们对展示广告、天气预报、提醒或产品推荐的看法，并公开讨论了他们的担忧和建议。焦点小组的讨论到此结束。

## 参与者

我们从一所大学校园招募了一些学生来参加焦点小组。总共有19名学生表示有兴趣参与，我们将他们分为三组。年龄21 ~ 31岁(M = 25.7, SD = 2.8)。第一组由四名女性和四名男性参与者组成，用英语进行。第二组由6名男性参与者组成，用德语进行。第三组由一名女性和四名男性组成，同样是用英语进行。


所有参与者都拥有一部智能手机和一台台式电脑或笔记本电脑，或者两者都有。9名(47.37%)受访者表示自己有平板电脑，10名(52.63%)受访者表示自己有电视。流媒体是参与者观看电影、电视剧和新闻的首选方式。参与者不仅在电视上观看视频，还在平板电脑和笔记本电脑上观看。当被问及最近一次收到的重要通知时，参与者提到了电子邮件、即时消息和日历通知。

## 结果

在接下来的章节中，我们将描述对创意创造和讨论部分的分析。


### 通知方式

为了分析参与者的想法，三位研究人员仔细研究了所有的草图，并推导出了区分它们的因素。之后，他们就一组因素达成一致，并根据这些因素描述每个草图。我们总共收集了46张纸，其中37张包含通知样式的草图，9张包含书面评论。19个草图中最受欢迎的通知样式是来自桌面和移动操作的toast通知样式。Toast通知覆盖了屏幕的一部分，通常由一个带有图标和两行或两行以上文本的框组成。在现有的操作系统上，这些通知通常只显示几秒钟，然后再次消失。在一些草图中提到，在toast通知消失后，屏幕上应该显示一个较不具侵入性的指示器，例如应用图标。在大多数草图中，toast通知被放置在屏幕的右上角或右下角。

第二个最受欢迎的建议是在屏幕的顶部或底部设置一个ticker样式。在6幅草图上发现了ticker样式的变体。图2b显示了屏幕底部的一个标记通知的草图，它从右向左滚动内容。虽然不完全相同，但这种风格类似于Android 5.0版本之前使用的通知标记，后者临时将屏幕顶部的状态栏替换为滚动接收到的消息内容的标记。在小组讨论中出现的一个问题是，这种风格将覆盖放在屏幕底部的字幕。

另一个被推荐了6次的选择是，只显示图标，类似于Android设备屏幕顶部的状态栏或桌面操作系统的系统托盘区。建议将这些图标放置在右上角或右下角，类似于toast通知。与会者提到，可以通过在图标上增加一个徽章来增强图标的功能，以指示某个应用程序的待处理通知数量。图2c显示了屏幕右下方的三个图标，带有显示通知数量的徽章。

第四类建议是在电视机的框架或底座上嵌入LED。这种变异在草图上被发现了5次。参与者建议LED可以根据发出通知的应用程序或通知的重要性来改变颜色。这个选项类似于智能手机上的通知led。

有嘉宾表示，应把电视用作智能家居枢纽，在不使用电视时全屏显示通知及其他资讯。另一名与会者建议使用水平分辨率较宽的屏幕面板，预留作通知用。这将允许在不覆盖内容的情况下在电视上持续发送通知流。除了通知样式之外，所有与会者都同意声音应该是完全可选和可配置的。此外，与会者同意通知应该与其他设备同步，因此在一台设备上取消通知也应该在其他设备上取消通知。

### 关切
与会者就电视上的通知提出了若干关切。一个问题是内容的闭塞。通知应该在一定程度上是透明的，这样就不会隐藏任何重要的东西。例如体育转播的字幕和记分牌。参与者担心在一部黑暗的电影中会出现明亮的弹出窗口。

每个焦点小组提出的另一个问题是，独自看电视与与他人一起看电视的区别。参与者不喜欢在和其他人一起看电视时显示发送者和信息的部分内容的通知。一位与会者将此与做报告的场景进行了比较，并表示他在做报告时总是谨慎地禁用所有通知。有人建议使用“家庭模式”，当和别人一起看电视时，可以隐藏内容或完全禁用通知。此外，与会者指出通知应该是上下文感知的。首先，如果有人在电视前，它应该被检测到，所以通知可以自动调整或关闭。此外，过多的通知也被认为是令人讨厌的，所以应该只显示重要的通知。此外，通知不应该在真正沉浸式的电影中显示，但在电影结束后或在慢速时刻的错过事件的总结是可以接受的。

在最后的讨论中，一些与会者表示，如果通知用于显示广告，他们将禁用通知。还有一些人提到，如果广告能让他们免费观看电影或电视剧，他们认为可以接受。推荐通知，例如正在观看的电影的续集目前正在电影院上映，被认为是可以接受的，只要不过度使用。与会者一致认为日历提醒可能是有用的。

## 总结和讨论

在本节中，我们描述了为了探索智能电视上通知的设计空间而进行的三个焦点小组的过程。焦点小组由四个部分组成，介绍轮，创意创造，开放讨论和结束讨论。在创意环节，参与者勾画出智能电视上可能的通知机制草图。对这些草图进行分类后，通知样式分为四类。最受欢迎的是toast通知，其次是ticker通知和图标通知。进一步的变化包括在电视框架或底座中嵌入led，并将电视作为智能家庭的中心。除了视觉线索之外，声音也可以发挥作用。然而，声音应该是可选的和可配置的。

# 在线调查
基于焦点小组的发现，我们进一步调查了智能电视通知中应该显示多少内容。为了从广泛的人群中获得结果，我们设计了一个在线调查。

因此，我们创建了五个具有不同信息量的通知变体。这些变体如图3所示。我们关注的是显示的信息量，而不是设计本身。因此，我们决定将所有通知显示为toast通知，因为这种风格在焦点小组中最受欢迎，在桌面设置中也很常见。焦点小组参与者的另一个偏好是将图片放在右上方或右下角。因此，我们在右上角显示了所有通知变量。我们决定在同一个场景显示变体。因此，我们为这五个版本制作了视频。每个视频播放相同的视频内容，每个视频25秒长。虽然视频播放了三个通知弹出，但所有版本的时间都是相同的，即在开始后的4秒、15秒和18秒。显示的通知分为邮件通知、即时消息通知和二次邮件通知。

在变体1中显示了一个通用的通知图标，图标上的徽章用于跟踪挂起的通知(图3a)。变体2使用特定应用程序的图标而不是通用图标，并简要显示了创建通知的应用程序的名称(图3b)。变体3的行为与第二个变体类似，但是消息的发送方也显示出来了(图3c)。此外，在变体4中，消息的摘录显示在发件人的下方，因此显示了大部分信息(图3d)。这四个变体在解散之前是持久的。变体5还显示发送方和消息摘录，但是没有留下任何图标(图3e)。

我们设计了一个在线调查来收集通知变体的反馈。这项在线调查是通过邮件列表、社交网络和在线社区进行的。

## 步骤
这项在线调查由参与者在他们的网络浏览器中回答，包括三个部分。首先，我们询问了参与者的人口统计数据、看电视行为和他们接收通知的设备。在第二部分，所有的通知变量由参与者打分。通知变量进行了平衡(以随机顺序显示)。对于每个通知变体，都会提供一个简短的文本描述文本和一个嵌入的YouTube视频。

在每种情况下，参与者被要求用李克特5分制对以下5个陈述从“非常不同意”到“非常同意”进行评分。
问题1：有了这个通知机制，我感觉我再也不会错过任何通知了。
问题2：这个通知机制为我提供了我想要的信息。
问题3：这个通知机制扰乱了我看电视的体验。
问题4：当我一个人看电视的时候，我觉得使用这个通知机制很舒服。
问题5：当我和别人一起看电视时，我觉得使用这个通知机制很舒服。

最后，参与者应该对这两个陈述进行评价:“对我来说，知道每个应用程序有多少个通知是很重要的。”最后，参与者可以对我们的通知变体进行评论。

## 参与者
共有167人(50名女性，117名男性)完成了调查。他们的年龄在15 - 76岁之间(M= 28.8，SD= 10.2)，其中58%为学生，35%为员工，7%为其他。这项在线调查有英语、德语和西班牙语三种版本。英语版本46次(27.54%)，德语版本105次(62.87%)，西班牙语版本16次(9.58%)。参与者的家庭规模有显著的差异。19.7%的受访者表示独自居住、25.1%与另一人合住、24.5%与三人合住、22.1%与四人合住及6.0%与五人或以上合住。2.3%的人没有说明他们的家庭规模。

我们的问题是“你平均每天有多少小时一个人看电视?”以及“你平均每天和别人一起看多少小时电视?”在表1中，我们展示了参与者的电视使用情况。


我们还询问参与者他们拥有什么样的设备，他们在哪些设备上接收通知，以及他们在哪些设备上阅读通知。可能的选择有智能手机、平板电脑、能上网的电视、不上网的电视、台式电脑、笔记本电脑、智能手表、健身追踪器，或者什么都不买。在智能手机、平板电脑和pc上，通知是吸引用户注意的一个众所周知的范例。目前的智能手表和健身追踪器通常与智能手机相连。图4显示了响应。95.81%的人拥有智能手机，57.49%的人拥有平板电脑，51.50%的人拥有联网电视，40.72%的人拥有不联网电视，61.08%的人拥有台式电脑，90.42%的人拥有笔记本电脑，14.97%的人拥有智能手表，11.38%的人拥有健身追踪器。一名与会者表示，他没有任何这些设备。一般来说，参与者在所有智能设备上接收和阅读通知，但智能电视是一个明显的例外。

## 结果
我们使用弗里德曼检验分析了五种情况的所有主观评分(图5)。我们还使用Friedman检验和Wilcoxon符号秩事后检验(应用Bonferroni校正)分析了每个评级的评级，得出p < 0.005的显著性水平。

(Q1)未遗漏通知:我们发现Q1有显著差异，χ 2 (4) = 115.020, p < .001。对于这一陈述，变体3 (M = 4.40, SD = 1.08)和变体4 (M = 4.40, SD = 1.13)获得了最高的评级，其次是变体2 (M = 4.07, SD = 1.22)，变体5 (M = 3.78, SD = 1.36)和变体1 (M = 3.38, SD = 1.34)。具有通用图标的变体的评级显著低于所有其他变体(1vs2 Z =−6.322,p < .001, 1vs3 Z =−7.436,p < .001, 1vs4 Z =−7.436,p < .001, 1vs5 Z =−2.860,p = .004)。变种5的评分明显低于变种3 (Z =−5.326,p < .001)和变种4 (Z =−5.464,p < .001)。

(Q2)提供所需信息:我们发现Q2有显著差异，χ 2 (4) = 123.015, p < .001。对于这一表述，变体3 (M = 3.99, SD = 1.29)得到了最高的评价，其次是变体4 (M = 3.96, SD = 1.28)，变体5 (M = 3.86, SD = 1.32)，变体2 (M = 3.45, SD = 1.36)和变体1 (M = 2.86, SD = 1.22)。同样，变量1的评分显著低于其他变量(1vs2 Z =−5.798,p < .001, 1vs3 Z =−7.922,p < .001, 1vs4 Z =−7.022,p < .001, 1vs5 Z =−6.953,p < .001)。此外，变体2(应用程序图标，无文本)的评分明显低于带有文本的变体，即变体3 (Z =−4.325,p < .001)和变体4 (Z =−3.409,p = .001)。

(Q3)干扰性电视体验:Q3差异有统计学意义，χ 2 (4) = 17.560, p < .001。对于这一表述，变体4获得了最高的干扰评级(M = 3.74, SD = 1.36)，其次是变体3 (M = 3.56, SD = 1.35)，变体2 (M = 3.49, SD = 1.37)，变体5 (M = 3.42, SD = 1.38)和变体1 (M = 3.38, SD = 1.40)。变体1，只显示一个通用图标，收到最低的干扰评级。带有发送者和消息摘录的变体4被评为明显比所有其他变体更令人不安(5vs4 Z =−3.533,p < .001, 2vs4 Z =−3.073,p = .002, 3vs4 Z =−3.018,p = .003, 1vs4 Z =−3.751,p < .001)。

(Q4)单因素:Q4差异有统计学意义，χ 2 (4) = 22.216, p < .001。对于这一陈述，变体5得到了最高的评价(M = 3.93, SD = 1.36)，其次是变体3 (M = 3.81, SD = 1.38)，变体2 (M = 3.78,SD = 1.35)，变体4 (M = 3.75, SD = 1.37)和变体1 (M = 3.41, SD = 1.38)。2-5型差异不显著。变种1的评分显著低于变种2 (Z =−3.398,p < .001)、变种3 (Z =−3.654,p < .001)和变种5 (Z =−4.014,p < .001)。

(Q5)与他人的舒适度:Q4差异有统计学意义，χ 2 (4) = 60.511, p < .001。对于这一陈述，变体2得到了最高的评价(M = 3.19, SD = 1.36)，其次是变体1 (M = 3.18, SD = 1.39)，变体3 (M = 2.89, SD = 1.26)，变体5 (M = 2.77, SD = 1.23)和变体4 (M = 2.59, SD = 1.10)。变异2与除变异1外的所有变异均有显著差异(2vs3 Z =−3.415,p = .001, 2vs5 Z =−4.108,p < .001, 2vs4 Z =−5.236,p < .001)。变异1与变异3 (Z =−3.059,p = .002)、变异5 (Z =−4.127,p < .001)和变异4 (Z =−5.008,p < .001)差异显著。变异3与变异4差异显著(Z =−3.636,p < .001)。

### 可选的评论
在线调查的最后一部分包括一个免费的文本框，允许参与者输入与之前的任务无关的评论。两名研究人员将西班牙语和德语的评论翻译成英语，并过滤掉没有可用反馈的评论。这产生了55条评论，随后根据其内容进行了分类。

13名参与者明确表示，他们在任何情况下都不会在电视上使用通知系统。两名参与者表示，他们在看电视时根本不想被打扰，因此让智能手机静音。另外三名参与者不反对通过电视接收通知。相反，他们表示，这取决于通知的重要性，而这反过来又取决于发送消息的紧迫性或人。来自7名参与者的一个有趣的评论类别区分了看电影和“娱乐节目”，例如智力竞赛节目，“你不需要积极关注节目就能跟着看”。两名参与者建议在看完电影后显示通知。

在调查中，我们询问参与者，与周围有其他人时使用这种通知风格相比，他们单独使用这种通知风格会感到多舒服。在自由文本框中，有5位参与者讨论了这个问题。他们提出了多种模式，可以根据周围的人数进行切换。一种模式将不受限制地显示通知，而“私有”模式将只显示通知提示。定制是13位与会者讨论的另一个主题。他们建议对视频中显示的通知和他们希望看到的整体选项进行更改，从通知的颜色到应该使用的屏幕角落。

## 总结和讨论
在本节中，我们描述了在线调查，其中我们评估了五种具有不同数量内容的通知变体。对于每一种通知变体，我们要求参与者对五个陈述进行评价，并询问他们喜欢和不喜欢什么。此外，我们还在一个文本框中询问他们对智能电视上的通知的一般反馈。参与者拥有许多智能设备，他们在这些设备上接收和阅读通知。然而，一个例外是电视和智能电视，大多数参与者没有收到或读取通知。

在线调查的结果表明，除了通知中的消息节选，参与者更喜欢看到发件人或发件人。如果没有任何指示符，并且只显示一个通用图标对参与者来说是不够的，那么参与者就会担心缺少通知。但是，持久指示符和在通知中显示更多文本会增加遮挡显示空间。因此，参与者表示，带有文本的变体对电视观看体验的干扰最大。我们测试的4个变体都留下了图标，不这样做可以减少文本造成的干扰。当单独观看时，参与者喜欢所有的变体，除了通用的应用程序图标。当和其他人一起观看时，参与者喜欢较少显示发送者或信息的变体。

# 实验室研究
在在线调查中，我们调查了智能电视通知中应该显示的内容数量。一个主要的结果是通知应该由用户定制。为了进一步研究这一方向，我们进行了一项实验室研究，参与者被要求定制祝酒通知。因此，我们在实验室中设置了一个有沙发和电视的房间(参见图6)。我们实现了一个应用程序，使我们能够在播放视频时向电视推送通知。根据在线调查的结果，有必要在独自观看和与他人一起观看的同时调查定制。因此，我们分两组进行实验室研究，一组单独观看，另一组与另一个未知的人一起观看。这样做是为了观察参与者是否会选择不同的设置。下面我们将描述这项研究及其结果。

## 设计
为了深入了解独自看电视和与他人一起看电视之间的区别，我们进行了一项受试者之间的研究。第一组(A组)的参与者独自坐在电视机前，第二组(B组)在研究人员在场的情况下观看视频。我们使用55英寸的飞利浦全高清电视连接到亚马逊Fire电视盒，以实现现实的电视体验。亚马逊Fire TV让我们能够在视频上方推送通知，也让参与者能够自定义通知。在线调查的另一个局限性是，我们创建了一个示例场景，导致通知对参与者没有意义。因此，我们为Android设备开发了一个智能手机应用程序，记录设备上显示的所有通知。因此，实验室研究中显示的所有通知都是参与者最近收到的通知。通知是从日志文件中随机选择的，从即时消息通知到系统消息不等。

对于实验室研究本身，我们开发了第二个安装在亚马逊Fire TV上的Android应用程序。这个应用程序是能够播放视频，同时显示覆盖与通知。此外，它允许用户使用九种不同的设置来控制通知的表示。设置菜单的GUI显示在图7的左侧。这些设置包括:位置、大小、图标、主题、不透明度、持续时间、内容、线条和声音。位置设置控制通知在屏幕上的显示位置，从左上到右下有九个可能的选项。大小设置允许缩放通知从小(225dp)，中等(300dp)到大(375dp)，使用Android的密度无关像素(dp)度量。图标设置允许显示应用程序的图标在全彩色和灰度，一个通用的应用程序图标在彩色和灰度，或根本没有图标。主题设置允许将通知的背景设置为白色(浅色主题)或黑色(深色主题)。不透明度可以设置为25%，50%，75%或100%。持续时间设置控制显示通知的时间，从1秒到25秒。内容设置控制显示多少日志文本。可能的选项是只显示应用程序的名称，包括标题/发件人，以及显示标题/发件人和消息。行设置取决于内容设置，因为它控制显示的行数，可能的值为1-5或无限。声音设置可以启用或禁用，启用时播放默认声音。

## 过程

我们两次邀请了参与者。第一次签署同意书并设置通知记录器。两天后，我们第二次邀请他们来我们的实验室。首先，我们要求他们填写一份人口统计数据表，并让他们坐在电视前的沙发上(屏幕与参与者之间相距3米)。然后我们解释说，我们为电视开发了一个应用程序，可以在播放《生活大爆炸》(Big Bang Theory)一集时，显示过去两天的随机通知。对于A组，研究人员明确表示，他们将独自观看这一集，房间里没有任何人。对于B组，研究人员会呆在房间里。我们打开设置屏幕，向参与者简要介绍了9个可用的设置。此时还没有配置任何设置。因此，参与者被要求自己探索设置。在配置完所有设置后，会出现一个预览通知，允许参与者进行进一步调整。当参与者认为通知的表达是合适的，我们就开始前半集的内容。对于A组，研究人员离开了房间。在预定的时间显示了10条通知。显示通知的预定义时间是由我们随机选择的，每个参与者都一样。上半场结束后，剧集暂停，设置页面自动打开。参与者有机会在这一集的后半部分改变他们的设置。后半部分显示了另外十份通知。在观看完完整集后，设置页面再次打开，参与者被要求再次调整设置。最后，我们要求参与者用李克特5分制对每个场景的重要性进行打分。

## 参与者

共有14名参与者(5名女性)参与了这项研究，他们都是在我们大学校园招募的。年龄22 ~ 32岁(M = 25.86, SD = 2.95)。其中12名参与者是学生，1名是博士生，1名是推动者。

## 结果

在图8中显示了对设置重要性的一致看法，突出显示了定制通知的必要性。定制通知的三个最重要的设置是位置(M = 4.79, SD = 0.43)、大小(M = 4.71, SD = 0.47)和内容(M = 4.50, SD = 0.65)。其次是持续时间(M = 4.29, SD = 0.83)、内容行数(M = 4.01, SD = 0.62)、不透明度(M = 3.93, SD = 1.14)、图标样式(M = 3.64, SD = 0.84)和声音(M = 3.50, SD = 1.83)。主题设置获得中性评分(M = 3.00, SD = 1.24)。然而，统计数据并没有显示单独观看或与他人一起观看的人之间有任何显著差异。根据参与者的最终设置，以下值是最受欢迎的。对于标称设置值，我们将报告模式，对于持续时间，我们将报告M和SD。这就产生了一种最流行的通知样式，如下所示:通知在右上角的一个黑色主题框中，显示时间为M = 4.93, SD = 2.6秒，不透明度为75%。包括一个彩色的应用程序图标，发送者和两/三/无限行消息，小字体，没有声音。可视化表示显示在图7的右侧。

位置:9人选择右上角的位置，2人选择左下角，2人选择右下角。两组间无显著差异。重要的是，通知的定位既要提供可见性，又不能隐藏内容或程序插入[P4, P8]。两名参与者认为，他们选择这个位置是因为他们习惯了用智能手机和笔记本电脑来做这个位置[P11, P12]。

大小:10个参与者选择小尺寸的通知，4个选择中尺寸的，没有一个选择大尺寸的。两组间无明显差异。通知应该足够大以便阅读，足够小以便不隐藏内容[P8]。太大的覆盖是令人讨厌的[P4, P14]，大小应该取决于电视的大小和距离[P2]。

图标:所使用的图标的选择取决于这两个组。与研究人员一起观看的参与者选择了一个图标，该图标属于即将到来的通知。5名参与者选择了应用程序图标的颜色，2名参与者使用了应用程序图标的灰度。单独观看的参与者选择了不同的图标。只有3名参与者选择了应用程序的彩色图标。两名参与者使用通用图标来显示传入的通知，另外两名参与者决定完全隐藏图标。应用图标的使用有助于判断通知的重要性，它生成了通知[P1, P3, P9, P10, P11]。

主题:十名参与者设置黑暗变体，四名参与者设置浅色变体。两个与会者提到对比很重要[P1, P4]，另外两个与会者认为光明和黑暗主题之间没有太大的区别[P9, P12]。

不透明度:单独观看的参与者都选择了高不透明度，其中6人使用75%的不透明度，1人使用100%的不透明度。在与一名研究人员一起观看的参与者中，一名参与者选择了25%的不透明度，两名参与者分别选择了50%、75%和100%。通知不要屏蔽电视内容[P8, P12]，不要太透明[P3, P12]。这个设置对减少分心很重要[P11]。一名与会者认为25%或50%的不透明度太透明[P3]，而另一名与会者则认为不透明度应在25%至50%之间，以免遮挡电视内容[P8]。

持续时间:单独观看的参与者选择更长时间来显示通知。一名参与者使用了3秒，一名参与者使用了4秒，4名参与者使用了5秒，还有一名参与者选择了13秒。然而，两名与研究人员一起观看的参与者选择了3秒。2个参与者使用4秒作为持续时间，3个参与者选择5秒作为持续时间。显示通知的持续时间的设置是在足够长以阅读消息和足够短以使通知不令人讨厌之间的平衡[P11]。对于持续时间也存在分歧。一个单独观看的参与者认为，超过10秒的通知显示时间太长了。然而，与研究人员一起观看的参与者评论说，显示通知2 - 3秒就足够了[P8]。另一位与会者认为应该有一个标准的持续时间，用户可以按一个按钮终止阅读或跳过[P2]。

内容:在单独观看的参与者中，1名参与者选择只显示发送者，6名参与者选择显示发送者和通知消息。在与一名研究人员一起观看的参与者中，4名参与者选择只显示发送者，3名参与者选择显示通知的发送者和消息。没有一个参与者选择只显示应用程序的名称。与会者表示，考虑到隐私问题，决定屏幕上应该显示什么很重要[P1, P8, P12]。有些人只想在手机上看通知[P2]，但另一些人可能想在电视上看通知[P2]。当更多的文本显示时，需要更长的注意力，所以你可能会错过你正在观看的内容[P9]，但也会影响你所了解的内容[P10]。

行数:在选择显示通知信息的9名参与者中，有3人分别选择了两行、三行和无限行。其中包括与一名研究人员一起观看的参与者，其中一名参与者选择了2行，另两名选择了3行。显示内容的长度也是一个隐私设置，取决于谁可以看到通知[P8, P10]。另一位与会者建议有意义地减少显示的内容，当全文对于一个简短的插入来说太多了[P4]。

声音:除一人外，所有与会者都关闭了传入通知的声音。他们认为这种声音毫无意义[P1]，没有必要[P2]，而且会分散注意力[P11]。三名参与者认为这种声音很烦人[P4, P10, P12]。一名参与者认为，声音可能会打扰一些人，但可能有助于记住在看完电视后对通知的行动[P9]。

## 总结和讨论

在本节中，我们描述了我们的实验室研究，我们邀请了14名参与者在看电视时定制通知。实验室研究揭示了明确的定制需求。参与者对所有设置的重要性进行了至少平均不同意或不同意的评价。我们还报告了关于所提供设置的定性反馈。此外，我们提出了最流行的设置配置，可作为进一步研究的初始设置。“与研究人员一起观察”方法的一个局限性是参与者和研究人员之间的关系。在未来的研究中，应该调查与朋友、家人或伴侣观看的差异。

# 设计指南

基于我们从焦点小组、在线调查和对照实验室研究中得到的结果，我们得出了以下关于电视通知的指导方针。开发者可以利用这些指南以一种有意义的方式来吸引用户对智能电视的注意力。

## 评估重要性

开发者应该评估通知的重要性，而不是像目前在其他智能设备上那样创建一个通知流。关于智能手机通知的相关研究表明，重要的通知是关于人物和事件[21]。从焦点小组和在线调查中获得的见解证实了这一点。对有些人来说，没有什么重要的事情能分散他们看电视时的注意力。正因为如此，智能电视上的通知应该总是可选的。

## 隐私方面的考虑

智能电视的隐私方面不同于其他智能设备。电视通常是共享设备，供多人使用，通常是同时使用。因此，与其他智能设备不同的是，不建议在通知中简单地显示消息摘要。在焦点小组中提出的一个想法是根据电视机前的人数使用多个资料。一个配置文件可以用来单独看电视，不受显示信息的限制。当你和别人一起看电视的时候，你可以使用另一个资料。在这个“私有”配置文件中，通知可以显示不同级别的信息。例如，不显示消息摘要、排除发件人或使用默认的应用程序图标。我们建议开发一个系统，可以检测到电视机前的人，并利用这一信息自动调整通知中显示的信息量。如果不可能采用自动化的解决方案，至少应该能够轻松地在公共模式和私有模式之间切换。

## 显示时机
这项在线调查的许多参与者提到，他们喜欢在电视上播放通知的想法。然而，在看电影时不应该显示通知，因为这被认为会分散注意力。相反，参与者建议在看完电影后显示通知。之前关于定时通知的工作已经表明，如果通知出现在任务之间[1]，那么通知就不会那么容易分心。除了电影的结束，我们建议在广告间歇时通知用户，在视频点播电影的情况下，在电影暂停时通知用户。

## 是微妙的

智能电视上的通知应该是微妙的。效果和动画应该小心使用，以避免分散用户的注意力。我们实验室研究的参与者不喜欢播放声音的想法。大小、不透明度、显示时长和文本长度必须达到平衡，以最大化可读性和最小化内容遮挡。

## 可定制
在所有的研究中，参与者都认为必须能够定制通知的显示方式。如上所述，要显示的信息量应该是可定制的。此外，通知在屏幕上的位置和显示时间是可配置的。

# 结论与未来工作

在本文中，我们开发了智能电视上的通知指南。通过三个焦点小组，我们收集了用户对电视通知的态度。设计空间包括通知的表示、显示的内容、引起通知的应用程序、接收到的通知的数量以及通知在屏幕上停留的时间。我们在网上调查中进一步研究了选定的设计方案，以获得更多关于智能电视上通知显示内容的信息。根据这些发现，我们实现了一个应用程序，使我们能够在播放视频时在电视上显示通知，并进行了实验室研究。在实验室研究中，我们调查了独自观看和与他人一起观看的场景的差异。根据这些发现，我们制定了在电视上显示通知的设计指南。只显示对用户真正重要的通知。此外，用户的隐私应该考虑，特别是当多人共享电视。通知可以主要在休息时间显示，以一种微妙的方式呈现。最后，用户应该能够轻松地自定义表示。

未来，可以通过在智能电视上安装一个显示通知的系统，并通过在人们的客厅安装该系统来进行实地研究，从而获得进一步的见解。特别值得注意的是，如果使用一种能够确定观众人数的系统，例如通过使用深度感应摄像机。系统可以根据观看者调整设置和显示的通知类型。此外，应该研究与智能电视上显示的通知交互的方法。重要的通知通常是关于消息的通知，因此用户可能希望他们可以使用智能电视直接对消息做出反应。另一个方向是环境可视化，以一种微妙的方式显示通知。一种可能的方法是使用Ambilight和IllumiRoom[13]等技术，它们可以在电视周围实现可视化。

# 引用
1. Piotr D. Adamczyk and Brian P. Bailey. 2004. 
If Not Now, when?: The Effects of Interruption at Different Moments Within Task Execution.
In Proceedings of the SIGCHI Conference on Human Factors in Computing Systems (CHI ’04).
ACM, New York, NY, USA, 271–278.
DOI:http://dx.doi.org/10.1145/985692.985727
2. Malek Alaoui and Myriam Lewkowicz. 2013.
A Livinglab Approach to Involve Elderly in the Design of Smart TV Applications Offering Communication Services.
In Proceedings of the 5th International Conference on Online Communities and Social Computing.
Springer-Verlag, Berlin, Heidelberg, 325–334.
DOI: http://dx.doi.org/10.1007/978-3-642-39371-6_37
3. Na Chang, Mhd Irvan, and Takao Terano. 2013.
A TV Program Recommender Framework.
Procedia Computer Science 22 (2013), 561–570.
DOI: http://dx.doi.org/10.1016/j.procs.2013.09.136
4. Cédric Courtois and Evelien D’heer. 2012.
Second Screen Applications and Tablet Users: Constellation, Awareness, Experience, and Interest.
In Proceedings of the 10th European Conference on Interactive Tv and Video (EuroiTV ’12).
ACM, New York, NY, USA, 153–156.
DOI: http://dx.doi.org/10.1145/2325616.2325646
