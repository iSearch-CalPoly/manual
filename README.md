# iSearch User Manual
CPE Capstone
Dandy Vo, Pixie Macke, Yezin Makhamreh
2022
![Cal Poly San Luis Obispo](https://imgs.search.brave.com/WDuA1EYwO3tk2_eJN1-PVhz968Eh_Txq0Y4JxCon_60/rs:fit:1200:1200:1/g:ce/aHR0cHM6Ly9zbG9j/aGFtYmVyLm9yZy93/cC1jb250ZW50L3Vw/bG9hZHMvMjAxNS8w/NC9DUFVfd29yZG1h/cmtfU0xPX2NwZ3Jl/ZW4uanBn)
# System Overview
## Frontend Codebase
iSearch consists of a frontend application that is developed in React.js and React Bootstrap. The codebase is found [here](https://github.com/iSearch-CalPoly/frontend). Only authorized developers can access and use this codebase. The various components of the frontend can be found below.

![User Dashboard](https://github.com/iSearch-CalPoly/manual/blob/main/dashboard.png?raw=true)
*Figure 1. User Dashboard*

![Operation Management Page](https://github.com/iSearch-CalPoly/manual/blob/main/operation.png?raw=true)
*Figure 2. Operation Management Page*

![Form Page](https://github.com/iSearch-CalPoly/manual/blob/main/form.png?raw=true)
*Figure 3. Form Page*
## Backend Codebase
iSearch uses Firebase as a backend service. This service provides the Firestore database, which is what we are using for form storage and processing. The codebase is found [here](https://github.com/iSearch-CalPoly/backend). Only authorized  developers can access and use this codebase.
![Firestore Databse](https://github.com/iSearch-CalPoly/manual/blob/main/firestore.png?raw=true)
*Figure 4. Firebase Database*
# Getting Started

## Cloning the repository 
Create a folder on your machine for this project and title it **iSearch**. 

Open the **iSearch** folder on you machine using Terminal, Command Prompt, or any othe command line interface. 

Git clone the frontend repository using the following commands (Note: These commands are specifically for for MacOS's Terminal)
```sh
git clone https://github.com/iSearch-CalPoly/frontend.git
```

If you are having trouble cloning you can consult the [GitHub Cloning a Reposiotry](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) documentation.


## Installing Node.js and npm
This project requires users to have Node.js and npm installed on their machine. 

If you don't have these installed already, follow the steps laid out in the [Downloading and Installing Node.js and npm documentation](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)

## Downloading and using an IDE
For this project, I highly recommend using an IDE tailored for JavaScript development.

You are allowed to use whichever IDE you prefer, however I would recommend using Visual Studio Code. 

To download Visual Studio code, refer to the [Visual Studio Code](https://code.visualstudio.com/docs) documentation.


## Using Git Version Control
For this project, we will be utilizing Git version control. If you do not already have a good understanding on how to use git, 
I highly advise you to view the following documentations as well as looking up Git best practices.
* [Git Book](https://git-scm.com/book/en/v2) 
  * Specifically, look into Git Basics, Git Branching, and merging.
* [Git Best Practices](https://sourcelevel.io/blog/7-git-best-practices-to-start-using-in-your-next-commit)
* [Creating a GitHub Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) 
  * **Important Note:** Never accept your own pull request. Have another team member review and accept it for you. If there are conflicts and you are unsure how to resolve them, contact a project manager.

# Developing a Form Page - Frontend
Once you have cloned the frontend repository, installed Node.js and npm, downloaded your preferred IDE, and brushed up on your Git knowledge, you can begin creating a form.

## Creating a new branch to house you work 
Before you begin creating a form, ensure that you are on the appropiate branch.

To check what branch you are currently on, you can use the following command:
```sh
git status
```

For work dedicated towards creating a form, there is a forms branch already created. If you are not already on this branch, you can use the following command: 
```sh
git checkout forms
```

Once you are on forms branch, you can the create your own subbranch to work in while you are developing your form. 
For example, if I am creating the SAR100 I would create a branch titled **sar100** using the following command:
```sh
git checkout -b sar100
```

After you have created your new branch you can begin working on creating your form. 

### Pushing Changes to your branch
As you make changes to your branch ensure that you are pushing your code to your branch. This will create a commit history and will allow you to go back to a specific commit if an error is to occur.

To push changes, follow these commands: (Note: I am in branch sar100 and I am pushing changes made to the sar100.js file
```sh
git add sar100.js
git commit -m "Write a useful commit message that can be used to idenetify what you adjusted for this commit"
git push origin sar100
```

### Merging into the forms branch and deleting your branch
Once you are finished creating the form that you are working on, push all the changes to your current branch.

After all the changes have been pushed, you can then create a new Pull Request. 

Once someone has reviewed and accepted your Pull Request, (i.e. your branch was successfully merged into the forms branch) you can delete the branch that you were developing in to keep our code space clean.

Once a branch is merged into the forms branch, all the commit history will be in that respective branch so don't worry about losing your history. 

The easiest way to delete a branch is through GitHub. 

**Note:** Please make sure that your branch is successfully merged into the forms branch before deletion. If you delete a branch before it is merged, you will lose all of your work.
If you are worried about this, contact a project manager when your branch is completed and a Pull Request is initiated and they can handle the rest for you. 


# Breaking Down sar100.js - Frontend

### Collapsed View
<img width="974" alt="Screen Shot 2022-03-17 at 1 49 19 PM" src="https://user-images.githubusercontent.com/46465233/158892806-3587d632-477b-45f6-a1ad-656d1da3d4a3.png">



### Expanded View
<img width="1367" alt="Screen Shot 2022-03-17 at 1 44 46 PM" src="https://user-images.githubusercontent.com/46465233/158892562-7607687c-b467-4dc2-a114-b7b9a84f9a30.png">



## Developing Form General Briefing - Generic Incident (SAR 100) - Frontend
When creating a new form, you will start off by creating a new file named after the form that you are creating. 

In this example, since we are creating the General Briefing - Generic Incident (SAR 100) form, you will create a file named **sar100.js**.

During the development process, you should only be making changes in the respective file that you created. Do not adjust any of the other 
files unless directed to or unless you have discussed with a project manager the reasons for adjusting other files. 

The frontend repository was designed in a way that you can reference other already created forms and reuse the code from those forms.
For example, the sar100.js file is already added to the respository. You can this file to create your respective form by copying and pasting the code from this file into yours and adjusting it to fit your needs.

## Reactstrap Components - Frontend
Our project will be utilizing components from Reactstrap that are already created. 

To look into the various componets that are used, you can reference the [Reactstrap](https://reactstrap.github.io/?path=/docs/components-card--card) documentation.

Specifically look into the following components
* [Card](https://reactstrap.github.io/?path=/docs/components-card--card)
* [Input](https://reactstrap.github.io/?path=/docs/components-forms--input)
* [Form](https://6-4-0--reactstrap.netlify.app/components/form/)

### Reactstrap Card Component
The [Card](https://reactstrap.github.io/?path=/docs/components-card--card) component is used to contain the various form fields specific to a section of a form.

For example, here is what the Incident Info card would look like: 

<img width="353" alt="Screen Shot 2022-01-31 at 5 22 44 PM" src="https://user-images.githubusercontent.com/46465233/151899455-b44b27a6-ae31-4d4e-baeb-1ed6e6dad2d6.png">

And here is the code used to create that Card:

<details><summary>Show Code</summary>

```js code
const IncidentInfo = ({formState, handleTextChange}) => {
    const [isOpen, setIsOpen] = useState(false)
    return(
        <Card style={cardStyles}>
            <CardBody >
                <div style={{display: "flex", alignItems: "center"}}>
                    <div onClick={() => setIsOpen(!isOpen)} style={{cursor: "pointer"}}>
                        {
                            isOpen ? 
                            <AiOutlineClose /> : 
                            <AiOutlinePlus/>
                        }
                    </div>
                    <CardTitle id="card-title" style={{flexGrow: "1", textAlign: "center"}}>
                        <b>Incident Info</b>
                    </CardTitle>                    
                </div>
                <Collapse isOpen={isOpen}>
                    <FormGroup>
                        <Label for="incidentName">
                            Incident Name
                        </Label>
                        <Input 
                        className="form-input"
                        type="text"
                        name="incidentName"
                        placeholder="Incident Name"
                        value={formState.incidentName}
                        onChange={e => handleTextChange(e)}
                        >
                        </Input>
                        <Label for="operationalPeriod">
                            Operational Period
                        </Label>
                        <Input 
                        className="form-input"
                        type="text"
                        name="operationalPeriod"
                        placeholder="Operational Period"
                        value={formState.operationalPeriod}
                        onChange={e => handleTextChange(e)}
                        >
                        </Input>
                        <Label for="incidentNumber">
                            Incident Number
                        </Label>
                        <Input 
                        className="form-input"
                        type="number"
                        name="incidentNumber"
                        placeholder="Incident Number"
                        value={formState.incidentNumber}
                        onChange={e => handleTextChange(e)}
                        >
                        </Input>   
                        <Label for="incidentSummary">
                            Incident Summary
                        </Label>
                        <Input 
                        className="form-input"
                        type="textarea"
                        name="incidentSummary"
                        placeholder="Incident Summary"
                        value={formState.incidentSummary}
                        onChange={e => handleTextChange(e)}
                        >
                        </Input>  
                    </FormGroup>
                </Collapse>
            </CardBody>
        </Card>
    )
}
```

</details>

### Reactstrap Card Component with Table Inputs
In addition to text fields and numeric fields, our application also supports table entries. An example of this can be seen in the Communication Plan card which looks like:
<img width="927" alt="Screen Shot 2022-03-17 at 2 01 12 PM" src="https://user-images.githubusercontent.com/46465233/158894497-9ef1791f-9572-40b6-a24b-a7a1bcf01f0f.png">

And here is the code used to create that Card:

<details><summary>Show Code</summary>

```js code
const CommunicationsPlan = ({formState, handleTextChange}) =>{
    const [isOpen, setIsOpen] = useState(false)
    return(
        <Card className="cardStyles">
            <CardBody >
                <div style={{display: "flex", alignItems: "center"}}>
                    <div onClick={() => setIsOpen(!isOpen)} style={{cursor: "pointer"}}>
                        {
                            isOpen ? 
                            <AiOutlineClose /> : 
                            <AiOutlinePlus/>
                        }
                    </div>
                    <CardTitle id="card-title" 
                    style={{flexGrow: "1", textAlign: "center"}}>
                        <b>Communications Plan</b>
                    </CardTitle>                    
                </div>
                <Collapse isOpen={isOpen}>
                    <FormGroup>
                        <Table responsive>
                            <thead>
                                <tr>
                                <th>
                                    Function
                                </th>
                                <th>
                                    Frequency
                                </th>
                                <th>
                                    Channel Description
                                </th>
                                <th>
                                    Channel
                                </th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                <th scope="row">
                                    Command (team -- base)
                                </th>
                                <td>
                                    <Input 
                                    className="form-input"
                                    type="text"
                                    name="commandFrequency"
                                    value={formState.commandFrequency}
                                    onChange={e => handleTextChange(e)}
                                    />                                
                                </td>
                                <td>
                                    <Input 
                                    className="form-input"
                                    type="text"
                                    name="commandChannelDescription"
                                    value={formState.commandChannelDescription}
                                    onChange={e => handleTextChange(e)}
                                    />    
                                </td>
                                <td>
                                    <Input 
                                    className="form-input"
                                    type="text"
                                    name="commandChannel"
                                    value={formState.commandChannel}
                                    onChange={e => handleTextChange(e)}
                                    />    
                                </td>
                                </tr>
                                <tr>
                                <th scope="row">
                                    Tactical (team -- team)
                                </th>
                                <td>
                                    <Input 
                                    className="form-input"
                                    type="text"
                                    name="tacticalFrequency"
                                    value={formState.tacticalFrequency}
                                    onChange={e => handleTextChange(e)}
                                    />    
                                </td>
                                <td>
                                    <Input 
                                    className="form-input"
                                    type="text"
                                    name="tacticalChannelDescription"
                                    value={formState.tacticalChannelDescription}
                                    onChange={e => handleTextChange(e)}
                                    />    
                                </td>
                                <td>
                                    <Input 
                                    className="form-input"
                                    type="text"
                                    name="tacticalChannel"
                                    value={formState.tacticalChannel}
                                    onChange={e => handleTextChange(e)}
                                    />    
                                </td>
                                </tr>
                            </tbody>
                        </Table>
                    </FormGroup>
                </Collapse>
            </CardBody>
        </Card>
    )
}
```

</details>

## Card Styles - Frontend
The styles for each card have been pulled from the respective [figma](https://www.figma.com/file/BsHNrqS66WfI4FpJmUcCjd/iSearch-Mockup?node-id=21%3A2) 
design and can be found at the top of the sar100.js file.

It should look something like this:
```js script
const cardStyles = {
    width: "100%",
    background: "#CEE5DE",
    marginTop: "calc(.3rem + .5vw)",
    borderRadius: "5px"
}
```

The cardStyles will be used to style each card. Make sure to use the same cardStyle for each card as it will allow for uniformity of each form. 


## Handling the States of Generic Input - Frontend

Since our web application involves a complex state logic, we will be using the react [useReducer](https://reactjs.org/docs/hooks-reference.html#usereducer) to handle 
the various states of each form page.

This involves creating a initial form state in our file that has all the names of all the Input fields that belong to the form. 

For example, the inital form state for the sar100 form would look like this:

```js script
const initialForm = {
    incidentName: "",
    operationalPeriod: "",
    incidentNumber: 0,
    incidentSummary: "",
    commandFrequency: "",
    commandChannelDescription: "",
    commandChannel: "",
    tacticalFrequency: "",
    tacticalChannelDescription: "",
    tacticalChannel: "",
    planSummary: "",
    preparedBy: "",
    datePrepared: "",
    timePrepared: ""
}
```

Each Input field for the form look something like this:

```js script
  <Input 
  className="form-input"
  type="textarea"
  name="incidentSummary"
  placeholder="Incident Summary"
  value={formState.incidentSummary}
  onChange={e => handleTextChange(e)}
  >
  </Input> 
```

Notice the **value** and **onChange** input fields. These must be included in each Input field that is created to allow for the state of this field to be handled.

Additionally, notice how the **name** field of the form, in this case _incidentSummary_, matches the name provided in the initialForm dictionary. 
It is required that the **name** field matches the name in the dictionary to allow reference to that specific Input field.

## Handling the States of Dynamic Input - Frontend

In addition to handling generic inputs, our application is also capable of handling dynamic input fields. A dynamic input field is a form field that has the ability to be added as many times as it is needed via an **Add** button. A dynamic input field can either add additional form input fields as well as additional rows to a table. Here is a gif to provide an example of what a dynamic input field looks like for both form fields and form tables:

![Screen Recording 2022-03-17 at 02 49 46 PM](https://user-images.githubusercontent.com/46465233/158900644-1b912e30-5a6d-4dd3-85ad-e9f23555bb4e.gif)

When working with dynamic input fields, we have to organize the initial form a little differently. In the initial form, dynamic fields will appear as a dictionary of the input fields that are added when the **Add** button is clicked. 

For example, the initial form state for sar104.js would look like this:

```js script
const initialForm = {
    incidentName: "",
    operationalPeriod: "",
    assignmentNumber: "",
    resourceType: "",
    dynamicFields: [
        {
            personnelName: "",
            personnelAgency: ""
        }
    ]
}
```

Notice how their is a field called **dynamicFields** that is associated to a dictionary containing the input fields **personnelName** and **personnelAgency**. By formatting the initial form state this way, we are able to handle capturing the inputs of each dynamic field that is added to the form. 


In addition to adjusting the initial form, we also have to adjust how the form card component looks in the code base as well. Here is an example from sar104.js that shows how we can handle populating newly added dynamic fields as well as handle capturing the input from the users: 

<details><summary>Show Code</summary>

```js code
const DynamicFields = ({obj, formState, dispatch, index}) => {
    return(
        <>
            <Label for={obj.personnelName}>
                Personnel Name
            </Label>
            <Input 
            className="form-input"
            type="text"
            name="personnelName"
            placeholder="Personnel Name"
            value={obj.personnelName}
            onChange={e => dispatch({
                type: "HANDLE DYNAMIC TEXT",
                field: e.target.name,
                payload: e.target.value,
                dynamicField: "dynamicFields",
                index: index
            })}/>       
            <Label for={obj.personnelAgency}>
                Personnel Agency
            </Label>
            <Input 
            className="form-input"
            type="text"
            name="personnelAgency"
            placeholder="Personnel Agency"
            value={obj.personnelAgency}
            onChange={
                e => dispatch({
                    type: "HANDLE DYNAMIC TEXT",
                    field: e.target.name,
                    payload: e.target.value,
                    dynamicField: "dynamicFields",
                    index: index
                })}
            />
        </>
    )
}

const PersonnelInfo = ({formState, dispatch, key}) => {
    const [isOpen, setIsOpen] = useState(false)
    const handleAdd = () => {
        dispatch({
            type: "ADD NEW FIELD",
            dynamicField: "dynamicFields",
            payload: {
                personnelName: "",
                personnelAgency: ""
            }
        })

    }

    return(
        <Card className="cardStyles">
        <CardBody >
            <div style={{display: "flex", alignItems: "center"}}>
                <div onClick={() => setIsOpen(!isOpen)} style={{cursor: "pointer"}}>
                    {
                        isOpen ? 
                        <AiOutlineClose /> : 
                        <AiOutlinePlus/>
                    }
                </div>
                <CardTitle id="card-title" style={{flexGrow: "1", textAlign: "center"}}>
                    <b>Personnel Info</b>
                </CardTitle>                    
            </div>
            <Collapse isOpen={isOpen}>
                <FormGroup>
                    {    formState.dynamicFields.map((obj, index) => (
                            <DynamicFields 
                            formState={formState}
                            dispatch={dispatch}
                            obj={obj} 
                            index={index}
                            />
                        ))
                    }
                <div style={{
                    marginTop: "calc(1vh + 1rem)",
                    display: "flex",
                    justifyContent: "space-between"
                }}>
                    <Button onClick={() => handleAdd()}
                    style={{background: "#00563A"}}>
                        Add
                    </Button>
                </div>
                </FormGroup>
            </Collapse>
        </CardBody>
    </Card>    
    )

}
```

</details>


## Putting it All Together - Frontend

After you have created all the various Cards with the appropriate input fields, you are ready to put the form together. 

To do this, you will need to make an constant named after your form. For the sar100 example, this const would be called SAR100 and should look something like this:

```js script
const SAR100 = () => {
    const[formState, dispatch] = useReducer(formReducer, initialForm)
    
    const handleTextChange = e => {
        dispatch({
            type: "HANDLE INPUT TEXT",
            field: e.target.name,
            payload: e.target.value
        })
    }

    const handleSubmit = (e) => {
        e.preventDefault()

        console.log(formState)
    }

    return(
        <div style={{
            marginRight: "calc(.75rem + 4vw)",
            marginLeft: "calc(.75rem + 4vw)",
            paddingTop: "70px"
            }}>
                <h1>
                    General Briefing - Generic Incident (SAR 100
                </h1>
            <form onSubmit={e => handleSubmit(e)}>
                <IncidentInfo 
                handleTextChange={handleTextChange}
                formState={formState}/>
                <CommunicationsPlan 
                handleTextChange={handleTextChange}
                formState={formState}/>
                <ActionPlanSummary
                handleTextChange={handleTextChange}
                formState={formState} />
                <PreparerInfo
                handleTextChange={handleTextChange}
                formState={formState} />
                <div style={{
                    marginTop: "calc(1vh + 1rem)",
                    display: "flex",
                    justifyContent: "space-between"
                }}>
                    <Button style={{background: "#00563A"}}>
                        Add
                    </Button>
                    <Button type="submit" style={{background: "#006CF5"}}>
                        Submit
                    </Button>
                </div>
            </form>
        </div>
    )
}

export default SAR100
```
# Security Rules - Backend
Security Rules are used to secure the database with user authentication and data validation.<br>

Data being written to the database is accessed with `request.data`, info on the user writing to the database is accessed with `request.auth`, and data already in the database is accessed with `resource.data`.<br>

Data types can be tested using the `is` condition. The supported data types are:
- `bool`
- `int`
- `float`
- `number`
- `string`
- `list`
- `map`
- `timestamp`
- `duration`
- `path`
- `latlong`


Keys of a map can be accessed as a list of strings using `data.keys()`.<br>
The length of a map, list, or string can be determined using `data.size()`.<br>

In `match` statements, the values in braces in the path are available as variables. If the variable name is followed by `=**`, it will match the remainder of the path, including subcollections.
```
match /collection/{documentId} {
    allow write: if documentId is string
}

match /collection/{document=**} {
    // Matches on /collection/documentId, /collection/documentId/subcollection/anotherId, etc.
}
```

External documents in the database can be accessed with `get(path)`, which fetches the document at the provided path, or `exists(path)`, which returns a boolean representing if a document exists at the provided path.<br>

The `request.method` variable is a string representing the CRUD operation: 'create', 'update', or 'delete'. Passing this argument allows for tests to be performed based on the operation the user is trying to commit. For example, the following condition can be used in to minimze fetches to other documents in the database.
```
(request.method == 'update' && request.data.field == resource.data.field) || request.data.field == get(/databases/$(database)/documents/incidents/$(incidentId)/collection/$(documentId)).data.field
```
This allows for the `get()` function, which is an external fetch, will only get called when a new document is created or, in the case of updating an existing document, the value of the field being written is different than what is already in the database.

## Writing Security Rules - Backend
Start with the following template:
```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    
    function validPeriod(period) {
      return period is map &&
             period.keys() == ['begin', 'end'] &&
             period.begin is timestamp &&
             period.end is timestamp &&
             period.end > period.begin;
    }
	  
    function validUser(auth, user) {
      return user is map &&
	         user.keys.hasOnly(['uid', 'name', 'phone', 'email') &&
	         user.uid == auth.uid &&
	         user.name == auth.displayName &&
	         (user.phone == null || user.phone == auth.token.phone) &&
	         (user.email == null || user.email == auth.token.email)
    }
    
    function validComments(comments, required) {
      return (required != true && comments == null) ||
             (comments is string && comments.size() <= 2048);
    }
  
    match /incidents/{incidentId} {
      match /<collection>/{documentId} {
        function auth<Document>R() {
          return false;
        }

        function auth<Document>W() {
          return false;
        }

        function valid<Document>() {          
          let preparedBy = validUser(request.auth, request.data.preparedBy)
        
          let comments = validComments(request.data.comments, false);

          return field1 && preparedBy && comments;
        }
        
        allow read: if auth<Document>R();

        allow create: if request.data.keys().hasOnly(['field1', 'field2', 'preparedBy', 'comments']) && 
                         valid<Document>() && 
                         auth<Document>W();

        allow update: if request.data.keys().hasOnly(['field1', 'field2', 'preparedBy', 'comments']) && 
                         valid<Document>() && 
                         authDocumentW();

        allow delete: if auth<Document>W();
      }
    }
  }
}
```
*Subject used as example document*<br>
Replace <<x>collection> in `match /<collection>/{documentId}` with your collection name. (should be plural of document name)
```
match /subjects/{documentId}
```

Replace <<x>Document> in `auth<Document>R()`, `auth<Document>W()`, and `valid<Document>()` with document name. (should be singular of collection name)
```
function authSubjectR() {}
function authSubjectW() {}
function validSubject() {}
```

In `valid<Document>W()`, test each field and store the condition in a variable. Then, after each field has been tested, return each variable ANDed together.<br>
If a JSON schema exists for the document, the conditions must match the data types of each field according to the schema.<br>
Optional fields must include a null condition, which will evaluate to `true` when the field is not present.
```
function validSubject() {
  let name = request.data.name is string
  let age = request.data.age == null || (request.data.age is int && request.data.age >= 0) // optional
  ...

  return name && age && ...
}
```

Under `allow create` and `allow update`, test for the keys in the data being submitted before calling `valid<Document>()` calling `request.data.keys().hasOnly([])`. The array passed to `hasOnly([])` is a list of all required and optional keys for the document. This allows for short circuit evaluation ensuring the data being written contains the proper fields before any potentially stateful checks need to be made. 
```
allow create: if request.data.keys().hasOnly(['name', 'age']) && validSubject() && authSubjectW()
```
# Troubleshooting Common Problems
### Can't Clone Repository
 1. Make sure that you have been added as a collaborator on the repository.
 2. GitHub no longer uses passwords for repository control, you must generate a token.
    - To generate a token, go to Developer Settings on your GitHub account.
    - See [GitHub Documentation](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
### Can't Compile Code
 1. Make sure that `package.json` is up to date with the repository.
 2. Make sure that `node_module` is up to date by running `npm install`.
 3. If there is an error, it is likely that there is a problem with the code, check the compiler messages for a clue as to what the problem is.
