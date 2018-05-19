## 영화정보 애플리케이션

##### overview
- 개요
  * server API 통신
  * 영화정보 보여주기
  * table view
  * collection view
- 프로젝트 진행 이유
  * 현업의 서비스와 가까워지기
  * 서버와 통신
    + URLSession 활용
    + Asynchronous programming
  * 지난 파트 습득 개념 총동원
  * 탭바 interface 활용
  * UIAlertController

##### Alert & ActionSheet
- UIAlertController class
  * major methods
    + init(title:message:preferredStyle:), func addAction(UIAlertAction), func addTextField(configurationHandler: ((UITextField)->Void)?=nil)
  * major property
    + title:String?, message:String?, actions:[UIAlertAction], preferredStyle[UIAlertControllerStyle]
    *[for more information about UIAlertController](https://developer.apple.com/documentation/uikit/uialertcontroller)*
- UIAlertAction class
  * major property
    + title:String?, isEnabled:Bool, style:UIAlertActionStyle
    *[for more information about UIAlertAction](https://developer.apple.com/documentation/uikit/uialertaction)*
- UIAlertActionStyle
  * default, cancel, destructive
- alert
  * warning needed before major action
  * need to provide chance for canceling action
  * check user's work once more or do work like deletion or announce for error
  * present important information decision is needed
- action sheet
  * multi action list that user can choose
  * open new working site or check stopped or not
  * set back user's decision or operation is not important

##### Tab Bar
- tab bar : use for conversion between categories or provide same information in various viewpoint
*[for more information about tab bars](https://developer.apple.com/ios/human-interface-guidelines/bars/tab-bars/)*
  * tab bar controller : control tab bar
  *[for more information about UITabBarController](https://developer.apple.com/documentation/uikit/uitabbarcontroller)*
  *[for more information about tab bar controllers](https://developer.apple.com/library/content/documentation/WindowsViews/Conceptual/ViewControllerCatalog/Chapters/TabBarControllers.html)*
  *[for more information about UITabBarControllerDelegate](https://developer.apple.com/documentation/uikit/uitabbarcontrollerdelegate)*
  * tab bar interface : compose interface using tab bar and tab bar controller
- tab bar structure
  * tab bar controller(tab bar view), contents view controller
- tab bar item
- tab bar delegate : monitor something related to tab and customize

##### URLSession & URLSessionDataTask
- URLSession : class provide API that give and take contents(data) through HTTP/HTTPS
*[for more information about URLSession](https://developer.apple.com/documentation/foundation/urlsession)*
*[for more information about URLSessionConfiguration](https://developer.apple.com/documentation/foundation/urlsessionconfiguration)*
- Request/Response
*[for more information about URLResponse](https://developer.apple.com/documentation/foundation/urlresponse)*
*[for more information about URL](https://developer.apple.com/documentation/foundation/url)*
- Session type
  * default, ephemeral, background session
- task
*[for more information about URLSessionTask](https://developer.apple.com/documentation/foundation/urlsessiontask)*
  * URLSessionDataTask : bring data object taking response data from server using HTTP methods
  *[for more information about URLSessionDataTask](https://developer.apple.com/documentation/foundation/urlsessiondatatask)*
  * URLSessionUploadTask : upload data object or file data through web server in application
  * URLSessionDownloadTask : download data from server and save as file type(can download in background state)
  *[about URL loading system](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/URLLoadingSystem/URLLoadingSystem.html)*
- ATS(App Transport Security) : function for security enforcement between application and web service
*[for more information about ATS](https://developer.apple.com/library/content/releasenotes/General/WhatsNewIniOS/Articles/iOS9.html)*
- ATS operation
  * give and take data using URLSession, CFURL, NSURLConnection
  * cannot do HTTP communication when ATS is active and cannot connect network which don't follow the requirement APPLE recommends
- glossary
  * TLS(Transport Layer Security) : password protocol
  * HTTPS(Hypertext Transfer Protocol Secure) : encrypted connection HTTP using TLS
- exception(ATS inactive)
  * streaming service through AVFoundation framework
  * request contents through WebKit
  * local network connection
  * until upgrade to recent TLS version for application maintenance

##### Grand Central Dispatch
- GCD(Grand Central Dispatch) : technique APPLE develops for optimized programming in multi-core and multi-processing condition
  * operation system manage thread pool -> programmer use task asynchronously
  *[for more information about dispatch](https://developer.apple.com/documentation/dispatch)*
  *[for more information about GCD](https://en.wikipedia.org/wiki/Grand_Central_Dispatch)*
  *[concurrency programming guide](https://developer.apple.com/library/content/documentation/General/Conceptual/ConcurrencyProgrammingGuide/Introduction/Introduction.html)*
- dispatch queue : perform task continuously or concurrently but execute in FIFO order
  * Serial Dispatch Queue : only one task per once
  * Concurrent Dispatch Queue : do task as much as can
  *[for more information about dispatch queue](https://developer.apple.com/documentation/dispatch/dispatchqueue)*
  *[for more information about dispatch qos](https://developer.apple.com/documentation/dispatch/dispatchqos)*
- dispatch source : C based mechanism for asynchronous handling specific type of system event
- operation queue : operate same as concurrent dispatch queue
  * can appoint maximum number of operation performed concurrently
  * various properties can use KVO(Key Value Observing)
  * can do moratorium, restarting, canceling operation

##### Notification Center & Notification
- notification : structure for delivering information through notification center in registered notification
*[for more information about notification](https://developer.apple.com/documentation/foundation/notification)*
- notification center : class delivers notification simultaneously to registered observer
  * stream flows synchronously
  * use NotificationQueue to use notification asynchronously
  *[for more information about notification center](https://developer.apple.com/documentation/foundation/notificationcenter)*
  *[for more information about notification queue](https://developer.apple.com/documentation/foundation/notificationqueue)*
