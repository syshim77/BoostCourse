## 기상정보 애플리케이션

##### overview
- 개요
  * JSON data
  * navigation controller
  * table view
- 프로젝트 진행 이유
  * table view 익히기
  * Swift-JSON 손쉽게 사용
    + JSON Encoder
    + JSON Decoder
  * storyboard segue
- 지난 시간 review
  * navigation interface
  * delegation design pattern

##### Table View
- table view
  * basic form
    + one column, multiple row, vertical scroll
    + each row action for one cell
    + divide row using section
    + header, footer -> add image or text
  * style
    + plain -> continuous
    + grouped -> grouped based on section
  * creation
    + dynamic prototypes -> design one cell and use to other cell's template
    + static cells -> own layout and fixed number of row
  * composite factor
    + cell, delegate, data source
    *[for more information about UITableView](https://developer.apple.com/documentation/uikit/uitableview)*
    *[table view programming guide](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/TableView_iPhone/AboutTableViewsiPhone/AboutTableViewsiPhone.html)*
    *[for more information about table views](https://developer.apple.com/ios/human-interface-guidelines/views/tables/)*
- table view cells
  * structure
    + contents area -> left side, input string or image or unique identifier
    + accessory view area -> right side, control objects(show detail, reorganize, switch)
  * basic function
    + UITableViewCell -> textLabel, detailTextLabel, imageView
  * custom table view cell
    + add subview to cell's content view
    + create UITableViewCell's custom subclass
    *[for more information about UITableViewCell](https://developer.apple.com/documentation/uikit/uitableviewcell)*
- datasource & delegate
  * datasource
    + adopt UITableViewDataSource protocol
    + provide information about table view creation and modification to table view object
    + data model's delegate
    + announce UITableView object the number of sections and rows
    + selectively implement row insertion, deletion, reorganization function
  * delegate
    + adopt UITableViewDelegate protocol
    + help table view's visual part modification, row's selective management, support accessory view, table view's individual row edition
    *[for more information about UITableViewDataSource](https://developer.apple.com/documentation/uikit/uitableviewdatasource)*
    *[for more information about UITableViewDelegate](https://developer.apple.com/documentation/uikit/uitableviewdelegate)*

##### Reuse View
- reusing principle
  * request view instance to data source -> look up reuse queue and if not empty then set new data, if empty then create new cell -> table view & collection view load cell on screen ->  if user scroll, some cell go into reuse queue -> repeat this process
  *[for more information about UITableView](https://developer.apple.com/documentation/uikit/uitableview)*
  *[for more information about UICollectionView](https://developer.apple.com/documentation/uikit/uicollectionview)*
  *[dequeueReusableCell(withIdentifier:for:) - UITableView](https://developer.apple.com/documentation/uikit/uitableview/1614878-dequeuereusablecell)*

##### Segue
- Segue : object that is used for screen conversion between view controllers in storyboard
*[for more information about UIStoryboardSegue](https://developer.apple.com/documentation/uikit/uistoryboardsegue)*
*[view controller programming guide using segues](https://developer.apple.com/library/content/featuredarticles/ViewControllerPGforiPhoneOS/UsingSegues.html)*
*[prepare(for:sender:) - UIViewController](https://developer.apple.com/documentation/uikit/uiviewcontroller/1621490-prepare)*

##### Codable
*[for more information about codable](https://developer.apple.com/documentation/swift/codable)*
- Encoding : 정보의 형태나 형식을 표준화, 보안, 처리 속도 향상, 저장 공간 절약 등을 위해서 다른 형태나 형식으로 변환하는 처리 혹은 그 처리 방식(부호화)
*[for more information about encodable](https://developer.apple.com/documentation/swift/encodable)*
- Decoding : invert performance of encoding
*[for more information about decodable](https://developer.apple.com/documentation/swift/decodable)*
- Encoder : device, circuit, software, algorithm for performing 부호화
- Codable = Decodable & Encodable
- CodingKey
  * enum type
  * use when JSON key name and struct property name is different
  *[for more information about codingkey](https://developer.apple.com/documentation/swift/codingkey)*
  *[encoding and decoding custom types](https://developer.apple.com/documentation/foundation/archives_and_serialization/encoding_and_decoding_custom_types)*
- JSONEncoder, JSONDecoder
*[for more information about JSONEncoder](https://developer.apple.com/documentation/foundation/jsonencoder)*
*[for more information about JSONDecoder](https://developer.apple.com/documentation/foundation/jsondecoder)*
*[using JSON with custom types](https://developer.apple.com/documentation/foundation/archives_and_serialization/using_json_with_custom_types)*
