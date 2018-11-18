# AddressBookWebapp
An address book JSF (JavaServer Faces) web app that stores and retrieves addresses from Java DB. JSF is a Java specification for building component-based UI for web applications.

# Description
The AddressBook Java DB contains an Addresses table with columns `ADDRESSID`, `FIRSTNAME`, `LASTNAME`, `STREET`, `CITY`, `STATE`, and `ZIP`.

Class `AddressBean` enables the AddressBook app to interact with the address book database. The class provides properties that represent an entry in the database and declares a `DataSource` for interacting with the database.

`index.xhtml` is the default web page for the AddressBook app. When this page is requested, it obtains a list of addresses from the `AddressBean` and displays them in tabular format using an `h:dataTable` element.

When the user clicks **Add Entry** in `index.xhtml` page, `addentry.xhtml` is displayed. When the user clicks **Save**, the input element's values are assigned to the properties of the `AddressBean` object and the `AddressBean` object's `save` method is invoked to store the new address in the database.

# Getting Started
## Prerequisites
- JDK 1.8
- Java EE 7.0
- Java DB - Apache Derby
- GlassFish Server 4.1

## Installing
- Creating a local respository.
```
git clone git@github.com:lnpeng/AddressBookWebapp.git
cd AddressBookWebapp
```

- Setting up the Database
  - Open the NetBeans IDE.
  - On the **Services** tab, expand the **Databases** node then right click **Java DB**. Select **Start** server to launch the Java DB server.
  - On the **Services** tab, expand the **Servers** node then right click **GlassFish Server 4.1**.Select **Start** to launch GlassFish.
  
- Creating the Database
  - On the **Services** tab, expand the **Databases** node, right click **Java DB** and select **Create Database...**.
  - Specify **Database Name**, **User Name**, **Password**.
  - Click **OK** to create the database.
  
- Populating the Database with sample data.
  - Expand the jdbc:derby://localhost:1527/addressbook node.
  - Right click the **Tables** node and select **Execute Command...** to open a **SQL** editor
tab in NetBeans. Add the SQL statements. Right click in the **SQL Command** editor and select **Run
File**.

## Running the tests
### Test the address book application
- Launch the application from a web browser.
- Check sample outputs.
- ![AddressBook](https://github.com/lnpeng/AddressBookWebapp/blob/master/Screen%20Shot%202018-11-18%20at%206.01.41%20PM.png)

# Build
- [Maven](https:maven.apache.org) - Dependency Management.
