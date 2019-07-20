## 회원가입 화면 구현
#### 부스트코스 iOS PJT2

##### overview
- 개요
  * autoLayout component
  * screen convert
    + navigation interface, modal
- 프로젝트 진행 이유
  * screen convert method
  * shared data management
  * design pattern understanding improvement
  * UIKit factor
    + Textfield, Datepicker, Human interface guidelines

##### H.I.G(Human Interface Guidelines)
- H.I.G content composition -> Overview, App Architecture, User Interaction, System, Capabilities, Visual Design, Icons and Images, Bars, Views, Controls, Extensions, Technologies, Resources  
*[for more information about H.I.G](https://developer.apple.com/ios/human-interface-guidelines/overview/themes/)*

##### Navigation Interface
- navigation interface : drill-down interface that used for screen convert of hierarchical structure
  * drill-down interface : interface that exist detail items for selectable items
  * compose navigation interface -> use storyboard, implement code  
  *[navigation - app architecture - iOS Human Interface Guidelines](https://developer.apple.com/ios/human-interface-guidelines/app-architecture/navigation/)*
- navigation controller : container view controller, use navigation stack, manage other view controller
  * navigation stack : like array can contain view controller
    + move screen in navigation stack -> can insert/delete view controller by using methods or segue  
    *[for more information about navigation controllers](https://developer.apple.com/library/content/documentation/WindowsViews/Conceptual/ViewControllerCatalog/Chapters/NavigationControllers.html)*  
    *[for additional information about navigation controller](https://developer.apple.com/documentation/uikit/uinavigationcontroller)*
- navigation bar  
*[for more information about navigation bar](https://developer.apple.com/documentation/uikit/uinavigationbar)*
- modal : screen convert technique(presenting)
  * presenting a view controller -> embed to container view controller, presentation
  * presentation and transition process -> presentation style, full-screen presentation style, popover style, current context style, custom presentation style, transition style
  * dismiss presented view controller -> call dismissViewControllerAnimated:completion: method  
  *[for more information about modal](https://developer.apple.com/ios/human-interface-guidelines/app-architecture/modality/)*  
  *[view controller programming guide for iOS: presenting a view controller](https://developer.apple.com/library/content/featuredarticles/ViewControllerPGforiPhoneOS/PresentingaViewController.html)*

##### View State Change Method
- Life Cycle -> viewDidLoad, viewWillAppear, viewDidAppear, viewWillDisappear, viewDidDisappear
- layout change method -> viewWillLayoutSubviews, viewDidLayoutSubviews  
*[UIViewController](https://developer.apple.com/documentation/uikit/uiviewcontroller)*

##### Delegation
- Delegation Design Pattern : provide function that one object can operate or control one another(interface control)
- datasource : data control
- protocol : can implement delegation and datasource  
*[for more information about delegation](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Protocols.html#//apple_ref/doc/uid/TP40014097-CH25-ID276)*  
*[for additional information about delegation](https://developer.apple.com/library/content/documentation/Swift/Conceptual/BuildingCocoaApps/AdoptingCocoaDesignPatterns.html#//apple_ref/doc/uid/TP40014216-CH7-ID8)*

##### Singleton
- SingleTon : guarantee object specific class's instance is only one(sharing the instance)
  * singleton design pattern -> FileManager, URLSession, NotificationCenter, UserDefaults, UIApplication  
  *[for more information about singleton](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/Singleton.html)*  
  *[for additional information about singleton](https://developer.apple.com/library/content/documentation/Swift/Conceptual/BuildingCocoaApps/AdoptingCocoaDesignPatterns.html#//apple_ref/doc/uid/TP40014216-CH7-ID177)*
- StackView : use interface layout in horizontal or vertical direction of many views  
*[for more information about stack view](https://developer.apple.com/documentation/uikit/uistackview)*

##### Target-Action design pattern
- Target-Action design pattern
  * target : object action will be called(basically controller)
  * action : method that will be called when specific event occur  
  *[for more information about target-action design pattern](https://developer.apple.com/library/content/documentation/General/Conceptual/Devpedia-CocoaApp/TargetAction.html)*  
  *[UIDatePicker](https://developer.apple.com/documentation/uikit/uidatepicker)*  
  *[Date](https://developer.apple.com/documentation/foundation/date)*  
  *[DateFormatter](https://developer.apple.com/documentation/foundation/dateformatter)*  
  *[introduction to data formatting programming guide for Cocoa](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/DataFormatting/DataFormatting.html#//apple_ref/doc/uid/10000029i)*  
  *[NSDateFormatter and Internet Dates](https://developer.apple.com/library/content/qa/qa1480/_index.html)*  
  *[Internationalization and Localization](https://developer.apple.com/library/content/documentation/MacOSX/Conceptual/BPInternational/Introduction/Introduction.html#//apple_ref/doc/uid/10000171i)*
- control event  
*[for more information about UIControlEvents](https://developer.apple.com/documentation/uikit/uicontrolevents)*  
*[for more information about UIControl](https://developer.apple.com/documentation/uikit/uicontrol)*  
*[for more information about controls](https://developer.apple.com/ios/human-interface-guidelines/controls)*

##### Gesture Recognizer
- Gesture Recognizer : recognize events about many gesture
  * UIGestureRecognizer -> UITapGestureRecognizer, UIPinchGestureRecognizer, UIRotationGestureRecognizer, UISwipeGestureRecognizer, UIPanGestureRecognizer, UIScreenEdgePanGestureRecognizer, UILongPressGestureRecognizer  
  *[for more information about UIGestureRecognizer](https://developer.apple.com/documentation/uikit/uigesturerecognizer)*  
  *[gestures - user interaction](https://developer.apple.com/ios/human-interface-guidelines/user-interaction/gestures/)*
- UITextField : editable text area in user interface
  * target-action design pattern, delegate object  
  *[for more information about text handling](https://developer.apple.com/library/content/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40009542)*  
  *[for more information about UITextField](https://developer.apple.com/documentation/uikit/uitextfield)*  
  *[for more information about UIResponder](https://developer.apple.com/documentation/uikit/uiresponder)*  
  *[understanding event handling, responders, and the responder chain](https://developer.apple.com/documentation/uikit/touches_presses_and_gestures/understanding_event_handling_responders_and_the_responder_chain)*  
  *[responder object](https://developer.apple.com/library/content/documentation/General/Conceptual/Devpedia-CocoaApp/Responder.html)*
