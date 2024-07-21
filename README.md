# Complete Java Course - Object-Oriented Programming - JavaFX App

###### @Author: MaurosMJ
<div style="text-align:center;">
    <img src="https://imgur.com/RbtbfGz.png" alt="Hibernate Logo" width="100" height="100">
</div>

This project is focused on building graphical user interfaces using JavaFX. The primary goals include understanding the fundamentals and structure of JavaFX, and familiarizing oneself with its main visual components.

**Technologies:**

- **DBMS Tool:** MySQL Workbench  
- **Dependencies:** mysql-connector-java, javafx libs 
- **Graphical user interface (GUI):** SceneBuilder

##### More Information:
**Course Link:** [Udemy Java Complete Course](https://www.udemy.com/course/java-curso-completo)  
**Section 25:** Graphical User Interface with JavaFX
**SceneBuilder:** https://gluonhq.com/products/scene-builder/

## Index

- [Overview](#overview) 
- [Key Points](#key-points)
- [Worknotes & Commits](#worknotes--commits)
- [Credits](#credits)

## Overview

JavaFX is the successor to Swing and Java AWT for creating graphical interfaces in Java. It supports development for desktop, web, and mobile platforms. JavaFX applications can be built using Java code or FXML. Post Java 11, JavaFX is no longer part of the JDK and needs to be downloaded separately from Gluon.

<div style="text-align:center;">
    <img src="https://imgur.com/ale4DWi.png">
</div>

## Key Points

- **MVC Pattern:** JavaFX follows the Model-View-Controller pattern.
  - **Model:** Manages domain data and logic.
  - **View:** Represents the user interface.
  - **Controller:** Handles user interactions and updates the view.
- **SceneBuilder:** A visual layout tool for designing JavaFX applications.
- **Eclipse Setup:** Instructions on setting up JavaFX SDK, installing E(fx)clipse plugin, and configuring SceneBuilder in Eclipse.
- **Creating JavaFX Projects:** Steps to create, configure, and run a new JavaFX project in Eclipse.
- **FXML and SceneBuilder:** Guide on creating and testing FXML files using SceneBuilder.
- **Event Handling:** Instructions for creating controllers to handle user events in JavaFX applications.
- **Additional Features:** Demonstrates creating utility classes, showing alerts, using TextFields, Labels, and ComboBoxes, and exploring main layout containers like AnchorPane, GridPane, SplitPane, VBox, HBox, BorderPane, and ScrollPane.


## Forms:

<div style="text-align:center;">
    <img src="https://imgur.com/fMgjVSY.png" alt="JPA Overview">
</div>

<div style="text-align:center;">
    <img src="https://imgur.com/V0QXoyi.png" alt="Entities">
</div>

<div style="text-align:center;">
    <img src="https://imgur.com/CiCjm37.png" alt="Entities">
</div>

<div style="text-align:center;">
    <img src="https://imgur.com/XrUmZPW.png" alt="Entities">
</div>

## Database:

<div style="text-align:center;">
    <img src="https://imgur.com/TYxtMZQ.png" alt="Entities">
</div>

<div style="text-align:center;">
    <img src="https://imgur.com/FoD6DFG.png" alt="Entities">
</div>

## Worknotes & Commits:

##### Worknote #1 - Created all entities and Maven dependencies
Commit hash: [58e882e2b2c386580d79a954e17b74c08874bebf](https://github.com/MaurosMJ/curso-javacompletoSimpleJPA-APP/commit/58e882e2b2c386580d79a954e17b74c08874bebf)  
**Checklist:**
* Classes: `Pessoa`, `Program`
* Maven Dependencies (pom.xml): mysql-connector-java, hibernate-entitymanager, hibernate-core  
* JPA database configuration: `persistence.xml`

##### Worknote #2 - Completed JPA mapping, performed code review, and tests
Commit hash: [31cd3ff3c8ed9f59d453b60c583e6c67bc6d894e](https://github.com/MaurosMJ/curso-javacompletoSimpleJPA-APP/commit/31cd3ff3c8ed9f59d453b60c583e6c67bc6d894e)  
**Checklist:**
* Created JPA mapping for entity `Pessoa`
* Created `EntityManagerFactory` in `Program` (Main class)
* Created `EntityManager` in `Program` (Main class)

## Credits:
This repository is maintained by [MaurosMJ](https://github.com/MaurosMJ). The Projects are based on the 'Java COMPLETO Programação Orientada a Objetos + Projetos' course.
