## 음원 재생기 어플리케이션

##### overview
- 개요
  * AVAudioPlayer class 사용
  * musicPlay application making
  * Xcode install
  * iOS programming 과정 체험
- 프로젝트 진행 이유
  * adapt to iOS programming environment
  * use for sub-material to review
  * autoLayout implement
  * large stream of iOS programming
  * MVC design pattern

##### Xcode
- installation & creating project
- Xcode 톺아보기  
*[for more information about Xcode](https://developer.apple.com/xcode/ide/)*  
*[for additional information about Xcode](http://help.apple.com/xcode/mac/current/)*

##### making application
- add image
  * Asset Catalog : auto-created folder named Assets.xcassets
    + manage various assets will be used in application
    + access easily to application resource by mapping(mapping -> file connection about asset and various devices' attribute)
    + ex) Groups, Assets, Attributes, Asset variations
    + contents type : Folders, JSON files, Content files  
    *[for more information about asset catalog](http://help.apple.com/xcode/mac/current/#/dev10510b1f7)*  
    *[for more information about asset catalog type](https://developer.apple.com/library/content/documentation/Xcode/Reference/xcode_ref-Asset_Catalog_Format/AssetTypes.html)*
  * app thinning : installation optimization technique
    + minimize installation capacity
    + speed up download
  * app slicing : create multiple piece of app bundle for various device and transmit appropriate piece to the device  
  *[add objects to the user interface](http://help.apple.com/xcode/mac/current/#/dev9ffcd0c51)*  
  *[add an outlet connection to send a message to a user interface object](http://help.apple.com/xcode/mac/current/#/devc06f7ee11)*  
  *[swift API design guidelines - Naming](https://swift.org/documentation/api-design-guidelines/#naming)*  
  *[menu command shortcuts (by menu)](https://developer.apple.com/library/content/documentation/IDEs/Conceptual/xcode_help-command_shortcuts/MenuCommands/MenuCommands014.html)*
- conntect interface builder's object with code(IBAction)
  * relation
    + event occur in control object, selected target's action is called
  * control event
    + defined UIControlEvents type
    + ex) touchDown, touchDownRepeat, touchDragInside, touchDragOutside, touchDragEnter, touchDragExit, touchUpInside, touchUpOutside, touchCancel, valueChanged, primaryActionTriggered, editingDidBegin, editingChanged, editingDidEnd, editingDidEndOnExit, allTouchEvents, allEditingEvents, applicationReserved, systemReserved, allEvents  
    *[for more information about UIControlEvents](https://developer.apple.com/documentation/uikit/uicontrolevents)*  
    *[for more information about Target-Action](https://developer.apple.com/library/content/documentation/General/Conceptual/CocoaEncyclopedia/Target-Action/Target-Action.html)*
- UIButton, UISlider, UILabel
  * UIButton
    + button, method connection -> addTarget method, @IBAction
    + state -> default, highlighted, focused, selected, disabled  
    *[for more information about UIButton](https://developer.apple.com/documentation/uikit/uibutton)*
  * UILabel
    + set property -> programming, storyboard inspector  
    *[for more information about UILabel](https://developer.apple.com/documentation/uikit/uilabel)*
  * UISlider
    + slider, method connection -> addTarget method, @IBAction
    + isContinuous property  
    *[for more information about UISlider](https://developer.apple.com/documentation/uikit/uislider)*
- implement
  * AVFoundation : framework that provide immense function such as handling & controling & calling & sending sound and video media  
  *[for more information about AVFoundation](https://developer.apple.com/documentation/avfoundation)*  
  *[for more information about AVAudioPlayer](https://developer.apple.com/documentation/avfoundation/avaudioplayer)*
  * Timer : provide function some moment time passed, transmit reserved message to specific object  
  *[for more information about Timer](https://developer.apple.com/documentation/foundation/timer)*  
  *[Xcode help - Write Code](http://help.apple.com/xcode/mac/current/#/dev8716704af)*

##### Cocoa Touch framework
- Cocoa Touch framework : iOS application developing environment
  * highest level framework
  * UIKit, Foundation  
  *[for more information about Cocoa](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/Cocoa.html)*
- UIKit : implement user interface and manage events
  * user interface -> View and Control, View Controller, Animation and Haptics, Window and Screen
  * user action -> Touch, Press, Gesture, Drag and Drop, Peek and Pop, Keyboard and Menu  
  *[for more information about UIKit](https://developer.apple.com/documentation/uikit)*
- Foundation : managed basic function of application by using original data type(String, Int, Double), collection type(Array, Dictionary, Set), operating system service
  * functional factor -> basic, application support, file and data management, networking  
  *[for more information about Foundation](https://developer.apple.com/documentation/foundation)*  
  *[for more information about swift standard library](https://developer.apple.com/documentation/swift)*

##### Auto Layout
- autoLayout : calculate size and location of all views in view hierarchy dynamically based on views' constraints
  * external changes, internal changes  
  *[for more information about auto layout](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/AutolayoutPG/index.html#//apple_ref/doc/uid/TP40010853-CH7-SW1)*  
  *[for more information about auto layout (code)](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/AutolayoutPG/ProgrammaticallyCreatingConstraints.html#//apple_ref/doc/uid/TP40010853-CH16-SW1)*
- External Changes
  * occur super view's size or shaped changed
  * ex) user use or not used iPad's Split View, device rotation, show or not show active call and audio recording bar, demand for different size of class, demand for different size of screen
- Internal Changes
  * occur user interface view's size or setting changed
  * ex) content show by application change, application globalization, application support dynamic type
- needs of autoLayout
  * attributes -> width, height, top, bottom, baseline, horizontal, vertical, leading, trailing, centerX, centerY
  * Safe Area
  * Constraint
    + define relation view self or between views through attributes
    + Constraint Priorities -> Content hugging priority, Content compression resistance priority
  * Anchor
  * Constraint designation method(implement) -> NSLayoutConstraint, Visual Format Language, Layout Anchor  
  *[for more information about auto layout (types of errors)](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/AutolayoutPG/TypesofErrors.html#//apple_ref/doc/uid/TP40010853-CH22-SW1)*  
  *[for more information about auto layout (visual format language)](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/AutolayoutPG/VisualFormatLanguage.html#//apple_ref/doc/uid/TP40010853-CH27-SW1)*
  * Constraint designation method(interface builder) -> Control-Dragging Constraints, Using the Stack & Align & Pin and Resolve Tools, Letting Interface Builder Create Constraints  
  *[constraints in interface builder](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/AutolayoutPG/WorkingwithConstraintsinInterfaceBuidler.html#//apple_ref/doc/uid/TP40010853-CH10-SW1)*  
  *[interface builder workflow](http://help.apple.com/xcode/mac/current/#/dev31645f17f)*  
  *[iOS H.I.G - adaptivity and layout](https://developer.apple.com/ios/human-interface-guidelines/visual-design/adaptivity-and-layout/)*



##### View Hierarchy
- View hierarchy  
*[creating and managing a view hierarchy](https://developer.apple.com/library/content/documentation/WindowsViews/Conceptual/ViewPG_iPhoneOS/CreatingViews/CreatingViews.html#//apple_ref/doc/uid/TP40009503-CH5-SW47)*
- superVIew, subview
- interface builder
- frame, bounds  
*[for more information about windows and views](https://developer.apple.com/library/content/documentation/WindowsViews/Conceptual/ViewPG_iPhoneOS/Introduction/Introduction.html)*

##### programming design pattern
- design pattern classification
  * purpose -> creational, structural, behavioral pattern
  * range -> class, object pattern  
  *[for more information about design pattern](https://en.wikipedia.org/wiki/Software_design_pattern)*  
  *[for more information about Singleton](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/Singleton.html)*
- Model-View-Controller(MVC)
  * model -> instance variable, accessor methods and properties, key-value coding, initialization and deallocation, object encoding, object duplication
  * view -> object that user can look
  * controller -> mediate between view and model object
    + coordination controllers -> direct and manage all or some function of application
    + view controller -> manage view  
  *[for more information about MVC design pattern](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/MVC.html)*  
  *[for additional information about MVC design pattern](https://developer.apple.com/library/content/documentation/General/Conceptual/CocoaEncyclopedia/Model-View-Controller/Model-View-Controller.html)*
