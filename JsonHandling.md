![JsonImage](/jsonImage.jpg)

# Handling Json in React

When working with large data units, there is every tendency there must be a logical data arrangement in the ecosystem.Making the streams of data to be parsed from one logic to another via the domination of data binding.
In this today's article, i will share with you how we can handle json in react.


## what is JSON?
JSON(Javascript Object Notation) - JSON is a text-based format mostly(.json files) used for storing and transferring data.JSON is a lightweight, text-based, language-independent data interchange format that is used to store and exchange data between different systems. It is one of the most popular data formats used in web applications and APIs.

            //JSON syntax
                {
                    "id" : "Emma",
                    "Occupation" : "Software Engineer",
                    "Salary" : "40,000"
                    "Currency" :"USD"
                }

## Why use JSON?
In web application, storing of data is occasionally done using the json format which stores data in a readable format.
It is easy to read and write, making it a great choice for data interchange between applications running on different platforms. JSON is also supported by most modern programming languages and is commonly used to send data over the web. JSON is often used as an alternative to XML (Extensible Markup Language)  due to its smaller size and faster parsing.

> - Note: JSON are always enclosed with arrays or objects(literals) when storing data.

        JSON Array - are enclosed in an array [].

        // let list an array of laptops and prices.
        ["MacBook", "price" "$20,000", "Dell","price" "$40,000",]



        
        JSON Objects - are enclosed in a curly brackets {}.

        // let list an object of laptops and prices.
        {"name" : "MacBook", "price" "$20,000", "Dell", "price" "$20,000"}

For more about
JSON objects and array visit here 👉<https://www.programiz.com/javascript/json>


# Prerequisites

Before we begin, these are technologies you should be familiar with and have installed on your local machine in order to follow up these guide:

> - Reactjs Knowledge
> - Javascript Knowledge
> - Nodejs v18+ already installed

# About Our Sample Application

For our sample application, we will create a simple list app of employees and their salaries every month. For more find the source code <>

# Create a Sample React app
Let start by running this in our terminal.

1. Open your terminal and run

        npx create-react-app reactapp



2. Navigate to the folder
        
        cd reactapp


3. Run

        npm start


![ReactApp](/ScreenshotReact.png "ReactApp")

Our App is now running locally..

4. Create a New folder and inside the folder create a (Employees.json) file. Our Json files would be stored there. 

![WorkerRule](/Group.png "WorkerRule")
 


5. Insert the code you see below, inside the Employees.json file.

                                [
                                {
                                        "id" : 0,
                                        "name" : "Emmanuel Umeh",
                                        "Occupation" : "Senior Software Engineer",
                                        "Salary" : "900,000",
                                        "currency" : "USD"
                                },

                                {
                                        "id":1,
                                        "name": "Rose Dublin",
                                        "Occupation" : "Lead Software Engineer",
                                        "Salary" : "900,000",
                                        "currency" : "USD"
                                },


                                {
                                        "id":2,
                                        "name": "Chinenye Amaka",
                                        "Occupation" : "Product Designer",
                                        "Salary" : "500,000",
                                        "currency" : "USD"
                                },

                                {
                                        "id":3,
                                        "name": "Mac Donald",
                                        "Occupation" : "Mobile App Developer",
                                        "Salary" : "900,000",
                                        "currency" : "USD"
                                }
                                ]


6. Create a Table.js file and Import the json file.

                                import lists from  "../src/Workers/Employees.json"


                                const Table = () => {
                                const JsonData = lists.map((JsonDatas) => {
                                        return(
                                        <tr>
                                                <td>{JsonDatas.id}</td>
                                                <td>{JsonDatas.name}</td>
                                                <td>{JsonDatas.Occupation}</td>
                                                <td>{JsonDatas.Salary}{JsonDatas.currency}</td>
                                        </tr>
                                        )
                                })
                                return(
                                        <>
                                        <table width="100%">
                                        <thead>
                                                <tr>
                                                <th>Sr.Number</th>
                                                <th>Name</th>
                                                <th>Jobs</th>
                                                <th>Salary</th>
                                                </tr>
                                        </thead>
                                        
                                
                                <tbody>
                                {JsonData}
                                </tbody>

                                </table>
                                        </>
                                )
                                }

                                export default Table;


7. Check your browser, we now have list of employees in our React App.

![TableImg](/TableReact.png "TableImg")


 Thanks for reading❤.
 
 Follow my twitter page for more <https://twitter.com/ElonLostSon>
