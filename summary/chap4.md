## 내 사진 관리 애플리케이션

##### overview
- 개요
  * photos framework
  * 사진앨범 구현
- 프로젝트 진행 이유
  * collection view 학습
    + collection view
    + collection view cell
    + collection view flow layout
  * 비동기 프로그래밍
    + operation
    + operation queue
  * UI component
    + scroll view
    + navigation item

##### Photos Framework
- photos framework : provide class that supports photo application, photo expand function
  * bring object and request change, observe change, support photos application's functions, asset and preview and caching, edit asset content
  * asset search & investigation
    + PHAsset, PHAssetCollection, PHCollectionList, PHCollection, PHObject, PHFetchResult, PHFetchOptions
  * asset contents loading
    + PHImageManager, PHCachingImageManager, PHImageRequestOptions, PHVideoRequestOptions, PHLivePhotoRequestOptions, PHLivePhoto
  * change request
    + PHAssetChangeRequest, PHAssetCollectionChangeRequest, PHCollectionListChangeRequest
  * asset contents modification
    + PHContentEditingInput, PHContentEditingOutput, PHAdjustmentData, PHContentEditingInputRequestOptions, PHLivePhotoEditingContext, PHLivePhotoFrame
  * observe change
    + PHPhotoLibraryChangeObserver, PHChange, PHObjectChangeDetails, PHFetchResultChangeDetails
  * operate with asset resource
    + PHAssetResource, PHAssetCreationRequest, PHAssetResourceCreationOptions, PHAssetResourceManager, PHAssetResourceRequestOptions
    *[for more information about photos](https://developer.apple.com/documentation/photos)*
    *[for more information about photos user interface](https://developer.apple.com/documentation/photosui)*

##### Concurrency & Asynchronous programming
- processor : hardware unit that performs program in computer at hardware side
  * ex) CPU
  * multiprocessor, dual-processor
  *[for more information about processor](https://ko.wikipedia.org/wiki/%ED%94%84%EB%A1%9C%EC%84%B8%EC%84%9C)*
  *[for more information about multiprocessing](https://ko.wikipedia.org/wiki/%EB%8B%A4%EC%A4%91_%EC%B2%98%EB%A6%AC)*
- core : main operation circuit
  * single-core, dual-core, multi-core
  *[for more information about core](https://ko.wikipedia.org/wiki/%EC%BD%94%EC%96%B4)*
- program vs process
  * program : code saved in back-up memory
  * process : work unit program and program status performed in memory
- thread : unit of work stream performed in one process
  * multi-threading
  *[for more information about thread](https://developer.apple.com/documentation/foundation/thread)*
- asynchronous programing
  * perform following job immediately without waiting
  * not wait for result
  * parallel
- concurrency programming
  * showed like performed concurrently
  * likely parallel
  * performed in rotation
  * both single-core, multi-core
- parallelism programming
  * performed exactly at the same time
  * data parallelism, task parallelism
  * only multi-core
  *[for more information about GCD](https://en.wikipedia.org/wiki/Grand_Central_Dispatch)*

##### Operation Queue
- operation : abstract class present data and code related to task
*[for more information about operation](https://developer.apple.com/documentation/foundation/operation)*
- operation queue : manage operation execution
  * cannot delete directly, have to stop operation
  *[for more information about operation queue](https://developer.apple.com/documentation/foundation/operationqueue)*
- operation object : operation class instance

##### Scroll View
- scroll view : able to scroll up, down, left, right and can maximize & minimize
*[for more information about UIScrollView](https://developer.apple.com/documentation/uikit/uiscrollview)*
*[for more information about UIScrollViewDelegate](https://developer.apple.com/documentation/uikit/uiscrollviewdelegate)*
*[scroll view programming guide](https://developer.apple.com/library/content/documentation/WindowsViews/Conceptual/UIScrollView_pg/Introduction/Introduction.html)*

##### Navigation Item
- navigation item : object show navigation bar contents
  * left, right bar button item, center title area
  *[for more information about UINavigationItem](https://developer.apple.com/documentation/uikit/uinavigationitem)*
- bar button item : special button arranged in UIToolbar or UINavigationBar
*[for more information about UIBarButtonItem](https://developer.apple.com/documentation/uikit/uibarbuttonitem)*
*[for more information about UIBarButtonSystemItem](https://developer.apple.com/documentation/uikit/uibarbuttonsystemitem)*
*[for more information about UIBarItem](https://developer.apple.com/documentation/uikit/uibaritem)*
*[system icons - icons and images](https://developer.apple.com/ios/human-interface-guidelines/icons-and-images/system-icons/)*

##### Collection View
- collection view : way to show sorted set of data items using flexible and modifiable layout
  * cell, supplementary views, decoration views, layout object
  * implement class & protocols -> top level containment, contents management, presentation, layout, flowlayout
  *[for more information about UICollectionView](https://developer.apple.com/documentation/uikit/uicollectionview)*
  *[for more information about collection views](https://developer.apple.com/library/content/documentation/WindowsViews/Conceptual/CollectionViewPGforIOS/Introduction/Introduction.html)*
- collection view cell
  * show data item on screen(one cell per one data item)
  * 2 background view, 1 contents view
  * cell layout managed by collection view layout object
  * support view reuse mechanism
  * not create instance directly, call dequeueReusableCell method
  *[for more information about UICollectionViewCell](https://developer.apple.com/documentation/uikit/uicollectionviewcell)*
- datasource : major object, must provided
*[for more information about UICollectionViewDataSource](https://developer.apple.com/documentation/uikit/uicollectionviewdatasource)*
- delegate : manage cell selection and emphasis, define method operating job for each cell, methods selectable
*[for more information about UICollectionViewDelegate](https://developer.apple.com/documentation/uikit/uicollectionviewdelegate)*
- UICollectionViewFlowLayout : layout object arrange cell in linear route and fill as much following this row
  * write flow layout object and point to collection view's layout object -> compose cell width and height -> control cell distance -> appoint size of header or footer -> set scroll direction
  *[for more information about UICollectionViewFlowLayout](https://developer.apple.com/documentation/uikit/uicollectionviewflowlayout)*
  *[for more information about UICollectionViewDelegateFlowLayout](https://developer.apple.com/documentation/uikit/uicollectionviewdelegateflowlayout)*
  *[collection view programming guide](https://developer.apple.com/library/content/documentation/WindowsViews/Conceptual/CollectionViewPGforIOS/Introduction/Introduction.html)*

##### Activity View Controller
- UIActivityViewController : help to use 내보내기 service easily
*[for more information about UIActivity](https://developer.apple.com/documentation/uikit/uiactivity)*
*[for more information about UIActivityViewController](https://developer.apple.com/documentation/uikit/uiactivityviewcontroller)*
- activity item : string, URL link, image, custom type instance following UIActivityItemSource protocols
*[for more information about UIActivityItemSource](https://developer.apple.com/documentation/uikit/uiactivityitemsource)*
*[for more information about UIActivityItemProvider](https://developer.apple.com/documentation/uikit/uiactivityitemprovider)*
