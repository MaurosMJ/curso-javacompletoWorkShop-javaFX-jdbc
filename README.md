# Complete Java Course - Object-Oriented Programming - JavaFX App

###### @Author: MaurosMJ

<div align="center">
    <img src="https://imgur.com/RbtbfGz.png" alt="FX Logo" width="100" height="100">
</div>

This project focuses on building graphical user interfaces using JavaFX. The primary goals are to understand the fundamentals and structure of JavaFX and familiarize oneself with its main visual components.

**Technologies:**

- **DBMS Tool:** MySQL Workbench
- **Dependencies:** mysql-connector-java, JavaFX libraries
- **Graphical User Interface (GUI):** SceneBuilder

### More Information
- **Course Link:** [Udemy Java Complete Course](https://www.udemy.com/course/java-curso-completo)
- **Section 25:** Graphical User Interface with JavaFX
- **SceneBuilder:** [Gluon Scene Builder](https://gluonhq.com/products/scene-builder/)

## Index

- [Overview](#overview)
- [Key Points](#key-points)
- [Worknotes & Commits](#worknotes--commits)
- [Credits](#credits)

## Overview

JavaFX is the successor to Swing and Java AWT for creating graphical interfaces in Java. It supports development for desktop, web, and mobile platforms. JavaFX applications can be built using Java code or FXML. Post Java 11, JavaFX is no longer part of the JDK and needs to be downloaded separately from Gluon.

<div align="center">
    <img src="https://imgur.com/ale4DWi.png" alt="JavaFX Overview">
</div>

## Key Points

- **MVC Pattern:** JavaFX follows the Model-View-Controller pattern.
  - **Model:** Manages domain data and logic.
  - **View:** Represents the user interface.
  - **Controller:** Handles user interactions and updates the view.
- **SceneBuilder:** A visual layout tool for designing JavaFX applications.
- **Eclipse Setup:** Instructions on setting up JavaFX SDK, installing the E(fx)clipse plugin, and configuring SceneBuilder in Eclipse.
- **Creating JavaFX Projects:** Steps to create, configure, and run a new JavaFX project in Eclipse.
- **FXML and SceneBuilder:** Guide on creating and testing FXML files using SceneBuilder.
- **Event Handling:** Instructions for creating controllers to handle user events in JavaFX applications.
- **Additional Features:** Demonstrates creating utility classes, showing alerts, using TextFields, Labels, and ComboBoxes, and exploring main layout containers like AnchorPane, GridPane, SplitPane, VBox, HBox, BorderPane, and ScrollPane.

## Forms

<div align="center">
    <img src="https://imgur.com/fMgjVSY.png" alt="Form Example 1">
    <img src="https://imgur.com/V0QXoyi.png" alt="Form Example 2">
    <img src="https://imgur.com/CiCjm37.png" alt="Form Example 3">
    <img src="https://imgur.com/XrUmZPW.png" alt="Form Example 4">
</div>

## Database

<div align="center">
    <img src="https://imgur.com/TYxtMZQ.png" alt="Database Example 1">
    <img src="https://imgur.com/FoD6DFG.png" alt="Database Example 2">
</div>

## Worknotes & Commits

#### Worknote #1 - Main view
Commit hash: [2c806dc3f2fe36121443a9650790649798144978](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/2c806dc3f2fe36121443a9650790649798144978)  
**Checklist:**
* Create FXML `MainView` (package `gui`)
* Load FXML in `Main`
* Update `Main.java`

#### Worknote #2 - Main view design 
Commit hash: [abe157529c323fbceb89e45794b8e2f9225b92aa](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/abe157529c323fbceb89e45794b8e2f9225b92aa)  
**Checklist:**
* Design `MainView.fxml`
* Customize menu items
* Update `Main.java`

#### Worknote #3 - Main view controller 
Commit hash: [7fdfde741cd569abd3e7640fe18a61fdf2a18817](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/7fdfde741cd569abd3e7640fe18a61fdf2a18817)  
**Checklist:**
* Create controller
* In view, associate controller, IDs, events

#### Worknote #4 - About view
Commit hash: [559d43b72b61c563292c5c3a8a557616fff8b5a1](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/559d43b72b61c563292c5c3a8a557616fff8b5a1)  
**Checklist:**
* Include utility classes to the project (`Alerts.java`, `Constraints.java`)
* Create `About.fxml` (VBox)
* In `Main.java`, expose `mainScene` reference
* In `MainViewController.java`, create `loadView` method

#### Worknote #5 - DepartmentList view design
Commit hash: [2851eda553b1dacae42af27971d22ee81732fa18](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/2851eda553b1dacae42af27971d22ee81732fa18)  
**Checklist:**
* Create `DepartmentList.fxml` (VBox)
* In `MainViewController.java`, load `DepartmentList`

#### Worknote #6 - DepartmentList controller
Commit hash: [e8fd2f7917031898efe422c3d543c2bd1b746516](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/e8fd2f7917031898efe422c3d543c2bd1b746516)  
**Checklist:**
* Create `model.entities.Department.java`
* Create `DepartmentListController.java`
* In view, associate controller, IDs, events

#### Worknote #7 - DepartmentService
Commit hash: [8048693c2ed9c7cc7b5b0f325f19408537cd943d](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/8048693c2ed9c7cc7b5b0f325f19408537cd943d)  
**Checklist:**
* Create `model.services.DepartmentService.java` with `findAll` method
* In `DepartmentListController`:
  * Create `DepartmentService` dependency with `set` method
  * Create `ObservableList<Department>`
  * Create `updateTableViewData` method

#### Worknote #8 - Initializing action as parameter 
Commit hash: [749c4995565286983f7d848572c5c71bb4bc6541](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/749c4995565286983f7d848572c5c71bb4bc6541)  
**Checklist:**
* Add a `Consumer<T>` parameter to `loadView` method
* After loading view, call `accept` from the `Consumer`
* Add a consumer instance on `loadView` calls

#### Worknote #9 - Adding database access 
Commit hash: [e1ac7e5ec529f73f358110f0f7789f4926d2e5a5](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/e1ac7e5ec529f73f358110f0f7789f4926d2e5a5)  
**Checklist:**
* Add `model.entities.Seller.java`
* Add `db.properties` to project
* In `DepartmentService`, add `DepartmentDao` dependency with Factory call
* Add data access packages to project:
  * `db`
  * `model.dao`
  * `model.dao.impl`

#### Worknote #10 - DepartmentForm (dialog) design 
Commit hash: [e721d356b4c29aba0dc49fe63ce7a3033086f78d](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/e721d356b4c29aba0dc49fe63ce7a3033086f78d)  
**Checklist:**
* Create `gui.util.Utils.java` with `currentStage` method
* In `DepartmentListController`, create `createDialogForm` method
* Call `createDialogForm` on "new" button action
* Create `DepartmentForm.fxml` (AnchorPane)
  * GridPane 3x3 (anchors: 20 top, 20 left)
  * ID text box: not editable
  * Label error: red
  * HBox (spacing: 5)

#### Worknote #11 - DepartmentFormController
Commit hash: [07d1a0d0e4dd93c2274717956ac94059213c1d28](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/07d1a0d0e4dd93c2274717956ac94059213c1d28)  
**Checklist:**
* Create `DepartmentFormController.java`
* In view, associate controller, IDs, events

#### Worknote #12 - Passing a Department object to DepartmentForm view 
Commit hash: [4472ecfd2206aec26d210cb3311051856fc39097](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/4472ecfd2206aec26d210cb3311051856fc39097)  
**Checklist:**
* In `DepartmentFormController`
  * Create a `Department` dependency with `set` method
  * Create `updateFormData` method
* In `DepartmentListController`
  * Update `onBtNewAction` method
  * Update `createDialogForm` method

#### Worknote #13 - Saving a new Department 
Commit hash: [b4e24462298269de9f58ef9c5aadf23ecf4cbf22](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/b4e24462298269de9f58ef9c5aadf23ecf4cbf22)  
**Checklist:**
* In `Utils`, implement `tryParseToInt` method
* In `DepartmentService`, create `saveOrUpdate` method
* In `DepartmentFormController`
  * Create a `DepartmentService` dependency with `set` method
  * Implement `onBtSaveAction`
  * Implement `onBtCancelAction`
* In `DepartmentListController`, inject `DepartmentService` instance

#### Worknote #14 - Observer design pattern to update TableView
Commit hash: [499f2512c4120780190216a03c2f2b03e8dbfe10](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/499f2512c4120780190216a03c2f2b03e8dbfe10)  
**Checklist:**
* Create interface `gui.listeners.DataChangeListener`
* In `DepartmentFormController` (subject)
  * Create `List<DataChangeListener>` dependency with `subscribe` method
  * Notify subscribers when needed
* In `DepartmentListController` (observer)
  * Implement `DataChangeListener` interface
  * Subscribe for `DepartmentFormController`

#### Worknote #15 - Validation exception
Commit hash: [c326d8154bc99511ce2e002a156fda7960ae6160](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/c326d8154bc99511ce2e002a156fda7960ae6160)  
**Checklist:**
* Create `model.exceptions.ValidationException`
* In `DepartmentFormController`
  * In `getFormData` method, implement verifications and throw `ValidationException`
  * Implement `setErrorMessages` method
  * In `onBtSaveAction`, call `setErrorMessages`

#### Worknote #16 - Editing Departments
Commit hash: [54f093c87f33813dc0149c5e24b6d1d9e40a74b7](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/54f093c87f33813dc0149c5e24b6d1d9e40a74b7)  
**Checklist:**
* Create `TableColumn<Department, Department>`, `TableCell<Department, Department>`
* In `DepartmentListController`, update `updateTableViewData` method
* Implement `createEditButton` method
* In `onBtNewAction`, set `id` = `null`

##### Worknote #17 - Seller TableView 
Commit hash: [e46008d0391a1b5497f703d9771da1f09edfa042](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/e46008d0391a1b5497f703d9771da1f09edfa042)  
**Checklist:**
* `gui.utils.Util.java`
  * `formatTableColumnDate` method
  * `formatTableColumnDouble` method
* `SellerListController`
  * `TableColumn` attributes (`Email`, `BirthDate`, `BaseSalary`) 
  * Update `initializeNodes`
* `SellerListView`
  * `TableColumn` (`Email`, `BirthDate`, `BaseSalary`) 
  * Associate `fx:id`

##### Worknote #18 - SellerForm
Commit hash: [dda801ae1877b8330931f4a158a6dd3447ecd6aa](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/dda801ae1877b8330931f4a158a6dd3447ecd6aa)  
**Checklist:**
* Clone `SellerFormController`
  * Replace: `Department` -> `Seller`
* Clone `SellerForm` view
  * Replace: `Department` -> `Seller`
* `SellerListController`
  * Uncomment `createDialogForm`

##### Worknote #19 - TextField & DatePicker
Commit hash: [ba786e741cef36e37b2c6fb988e451e35c992f97](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/ba786e741cef36e37b2c6fb988e451e35c992f97)  
**Checklist:**
* `gui.utils.Util.java`
  * `formatDatePicker` method
* `TextField` & `DatePicker` attributes (`Email`, `BirthDate`, `BaseSalary`)
* `Label` error attributes (`Email`, `BirthDate`, `BaseSalary`)
* Edit `SellerFormView`
* Bugfix: `SellerDaoJDBC.instantiateSeller`
  * `obj.setBirthDate(new java.util.Date(rs.getTimestamp("BirthDate").getTime()));`
* Update: `initializeNodes`
* Update: `updateFormData`

##### Worknote #21 - Department ComboBox 
Commit hash: [aaf32e4d7c543d883c72bcd80ef74f0ee3c66f50](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/aaf32e4d7c543d883c72bcd80ef74f0ee3c66f50)  
**Checklist:**
* Update controller:
  * `DepartmentService` dependency
    * attribute
    * set method
  * `ComboBox<Department>` `comboBoxDepartment`
  * `ObservableList<Department>` `obsList`
    * `loadAssociatedObjects`
  * `initializeComboBoxDepartment`
  * `updateFormData`
* Update view:
  * `ComboBox`
  * `fx:id`

##### Worknote #22 - Saving Seller 
Commit hash: [3ee145a6cbb32de4058424d637fc3fec477a5bb9](https://github.com/MaurosMJ/curso-javacompletoWorkShop-javaFX-jdbc/commit/3ee145a6cbb32de4058424d637fc3fec477a5bb9)  
**Checklist:**
* Update: `getFormData`
* Update: `setErrorMessages`

## Credits:
This repository is maintained by [MaurosMJ](https://github.com/MaurosMJ). The Projects are based on the 'Java COMPLETO Programação Orientada a Objetos + Projetos' course.
