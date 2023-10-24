<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To-do-list</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/brands.min.css">
    <link rel="stylesheet" href="styles.css">
    <style>
        :root{
    --p1-color:#d1453b;
    --p2-color: #eb8909;
    --p3-color: #246fe0;
    --p4-color: #666;

}
*{
    padding: 0;
    margin: 0;
}
.body{
    display: flex;
    justify-content: space-between;
    position:relative;
    margin: 16px auto;
    
}
nav{
    width: 20%;
    background: linear-gradient(to bottom, rgb(255, 255, 255),rgb(238, 240, 236));
    margin:0px 5px;
    padding: 18px;
    height: 91vh;
    position: relative;
    
}
.profile{
    display: flex;
    align-items: center;
    margin-top:0.5vh;
}
.profile-link{
    display: flex;
    align-items: center;
    margin-left: 15px;
    font-size: 18px;
}
.profile-image{
    border-radius: 50%;
    background-color:rgb(240, 232, 232) ;
    height:45px ;
    width: 45px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.profile-image img{
    border-radius: 50%;
    margin-top: 4px;
    height:31px;
    width: auto;
    background-color: white;
}
.float-right{
    display: flex;
    align-items: center;
}
section{
    width: 80%;
    /* background-color: green; */
}
a{
    text-decoration: none;
}
.btn-add-task{
    margin:3vh auto;
}
.btn-add-task input{
    background-color: rgb(238, 4, 82);
    color:white ;
    border: none;
    font-size: 15px;
    text-align: center;
    padding: 8px;
    border-radius: 3px;
    width: 100%;
}
.nav-item{
    margin-top:12px;
    font-size: 18px;
}
.nav-item i{
    
}
.nav-item text{
    padding-left:15px;
    color:black ;
}
.projects{
    margin-top: 35px;
    background-color: rgb(255, 170, 170);
    padding: 8px;
    border-radius: 3px;
    width: 95%;
}
.projects a{
    text-decoration: none;
    color: black;
}
.projects-btn{
    display: flex;
    align-items: center;
}
.btn{
    margin-left: auto
}
.fa-plus, .fa-chevron-left{
    margin-left:3px ;
}

/* Add task section */
.add-task{
    /* background-color: blueviolet; */
    margin: 2px 1vh;
    position: relative;
}
.add-task-section{
    padding: 7vh 7vh 2vh 7vh;
    margin:0 4vh ;
    /* background-color: pink; */
}
.add-task-header{
    display: flex;
}
.add-task-header{
    /* background-color: yellow; */
    margin: auto;
    display: flex;
    justify-content: space-between;
}
.btn-add-task button{
    background-color: var(--p1-color);
    border: none;
    padding: 10px;
    border-radius: 6px;
    font-size: 15px;
    width: 100%;
    color: white;
    
}
.sub-header{
    margin: 8px 0;
}
.setting{
    color: gray;
    font-size: 18px;
}
.setting text{
    margin-left: 6px;
}
.search-project input{
    padding: 8px;
    border-radius: 5px;
    width: 100%;
    border: solid gray 1px;
}
.sub-header{
    margin-bottom: 25px;
}
.add-active-project-section{
    /* background-color: yellow; */
    display: flex;
    justify-content: space-between;
    margin:0vh 9vh;
}
.active-project button{
    border: none;
    padding: 6px;
    border-radius: 6px;
    background-color: wheat;
    float: left;
    margin-left: 16px;
}
.add-project button{
    border: none;
    padding: 6px;
    border-radius: 6px;
    background-color: gray;
    float: right;
    color: white;
}
.modal{
    display: none;
    position:fixed;
    top: 0;
    width: 100%;
    height: 100%;
    /* background-color: yellow; */
}
.modal-content{
    margin: 5% 25%;
    padding: 20px;
    /* border: 1px solid #888; */
    width: 50%;
    box-shadow: 10px 10px 10px 10px rgba(0, 0, 0, 0.2);
    background-color: #fdfdfd;
}
.popup-heading{
    margin-top: 12px;
    margin-bottom: 12px;
}
.popup-form .name{
    border: none;
    padding: 10px;
    background-color: #f3eeee;
    color: black;
    margin-bottom: 5px;
    border-radius: 6px;
    width: 95%;
}
.popup-description{
    margin-top: 8px;
    margin-bottom: 8px;
}
.btn-modal{
    padding: 5px;
    margin-left: auto;
    margin-bottom: 8px;
}
.btn-modal input{
    padding: 8px;
    border-radius: 8px;
}
.btn-modal select{
    padding: 8px;
    border-radius: 8px;
}
.due-date{
    border: gray;
    background-color: #f3eeee;
}
.priority{
    border: none;
    background-color: #f3eeee;
}
.btn-popup{
    margin: 12px auto;
}
.btn-popup button{
    border: none;
    padding: 8px;
    border-radius: 8px;
}
.popup-cancel{
    background-color: red;
    color: white;
    padding: 8px;
}
.popup-add-task{
    background-color: green;
    color: white;
    padding: 8px;
}
.pop-up-search{
    display: none;
    position:fixed;
    top: 0;
    width: 100%;
    height: 100%;
}
.search-content{
    margin: 5% 25%;
    padding: 20px;
    /* border: 1px solid #888; */
    width: 50%;
    box-shadow: 10px 10px 10px 10px rgba(0, 0, 0, 0.2);
    background-color: #fdfdfd;
    height: 50vh;
    align-items: center;
    text-align: center;
}
.search-close{
    float: right;
    border: none;
    font-size: 25px;
    background-color: white;
    color: var(--p4-color);
}
.search-content input{
    border: none;
    /* background-color: var(--p4-color); */
    padding: 10px;
    width: 95%;
    border-radius: 8px;
}
.search-popup-description{
    margin-top: 6px;
    float: left;
    margin-left: 13px;
}
/* Today in Nav bar  */
.popup-today{
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    /* background-color: yellow; */
}
.today-content{
    margin: 5% 25%;
    padding: 20px;
    /* border: 1px solid #888; */
    width: 50%;
    box-shadow: 10px 10px 10px 10px rgba(0, 0, 0, 0.2);
    background-color: #fdfdfd;
}
/* edit and delete btn */
.edit-btn{
    background-color: green;
    color: white;
    border: none;
    padding: 5px;
    border-radius: 3px;
    font-size: 15px;
    /* margin-left: 5%;a */
    float: right;
    position: relative;
    
}
.delete-btn{
    margin-right: 1%;
    border: none;
    background-color: red;
    color: white;
    padding: 5px;
    border-radius: 3px;
    font-size: 15px;
    float: right;
    position: relative;
}
    </style>

    <script src="script.js"></script>
</head>

<body>
    <div class="body">
        <nav>
            <div class="profile">
                <a href="#">
                    <div class="profile-image profile-link">
                        <a href="">
                            <img src="image/mes.png">
                        </a>
                    </div>
                    <div class="profile-name profile-link">
                        <a href="#">
                            <p>Praman</p>
                        </a>
                    </div>
                    <div class="down-arrow profile-link">
                        <a href="">
                            <i class="fa-solid fa-angle-down"></i>
                        </a>
                    </div>
                </a>
                <div class="float-right">
                    <div class="notification profile-link">
                        <a class="notification-bell" href="">
                            <i class="fa-regular fa-bell"></i>
                        </a>
                    </div>
                    <div class="open-close-bar profile-link">
                        <a class="notification-bell" href="">
                            <i class="fa-regular fa-bell"></i>
                        </a>
                    </div>
                </div>
            </div>
            <div class="btn-add-task ">
                <button type="submit" id="add-task-btn">+ Add Task</button>
            </div>
            <div class="nav-links">
                <div class="search-link profile-link nav-item">
                    <a href="#" id="pop-up-search-btn">
                        <i class="fa-solid fa-magnifying-glass" style="color:#666;"></i>
                        <text class="search">
                            Search
                        </text>
                    </a>
                </div>
                <div class="inbox profile-link nav-item">
                    <a href="#">
                        <i class="fa-solid fa-inbox" style="color:#246fe0;"></i>
                        <text class="search">
                            Inbox
                        </text>
                    </a>
                </div>
                <div class="calandar profile-link nav-item">
                    <a href="#" class="today-btn" id="today-btn">
                        <i class="fa-regular fa-calendar" style="color:#eb8909;"></i>
                        <text class="search">
                            Today
                        </text>
                    </a>
                </div>
                <div class="filter-label profile-link nav-item">
                    <a href="#">
                        <i class="fa-solid fa-calendar-days" style="color:rgb(9, 197, 9);"></i>
                        <text class="search">
                            Upcoming
                        </text>
                    </a>
                </div>
            </div>
            <div class="projects">
                <a class="projects-btn" href="#">
                    <text class="project-text">Projects</text>
                    <div class="btn">
                        <i class="fa-solid fa-plus"></i>
                        <i class="fa-solid fa-chevron-left"></i>
                    </div>
                </a>
            </div>
        </nav>
        <section class="add-task">
            <div id="form-placeholder"></div>
            <div class="add-task-section">
                <div class="add-task-header">
                    <h2>Projects</h2>
                    <setting>
                        <a class="setting" href="">
                            <i class="fa-solid fa-gear"></i>
                            <text>Settings</text>
                        </a>
                    </setting>
                </div>
                <p class="sub-header">Your workspace</p>
                <div class="search-project">
                    <input type="text" class="search-space" placeholder="Search Projects">
                </div>
            </div>
            <div class="add-active-project-section">
                <div class="active-project">
                    <button href="#">Active Project</button>
                </div>
                <div class="add-project">
                    <button href="#">
                        Add Project
                    </button>
                </div>
            </div>
        </section>
    </div>
    <div id="popup" class="modal">
        <div class="modal-content">
            <span id="close-popup-button" class="close">&times;</span>
            <h2 class="popup-heading">Popup Form</h2>
            <form class="popup-form" id="popup-form">
                <!-- Your form fields go here -->
                <input type="text" class="name" id="name" name="name" placeholder="Task Name" required>
                <p class="popup-description">Description</p>
                <div class="btn-modal">
                    <input class="due-date" type="date"></input>
                    <select class="priority">
                        <option value="Priority 1">Priority 1</option>
                        <option value="Priority 2">Priority 2</option>
                        <option value="Priority 3">Priority 3</option>
                        <option value="Priority 4">Priority 4</option>
                    </select>
                </div>
                <div class="btn-popup">
                    <button class="popup-cancel">Cancel</button>
                    <button class="popup-add-task" id="submit" name="" submit>Add Task</button>
                </div>
            </form>
        </div>
    </div>
    <div id="popupsearch" class="pop-up-search">
        <div class="search-content">
            <button id="search-close" class="search-close">x</button>
            <input type="text" name="search" id="search-popup" placeholder="What would you like to do?">
            <hr>
            <p class="search-popup-description">Recently searched</p>
        </div>
    </div>
    <!-- Today display -->
    <div id="popuptoday" class="popup-today">
        <div class="today-content">
            <button id="today-close" class="today-close">x</button>
            <div id="results-container">
                <div id="results-list"></div>
            </div>
        </div>
    </div>


    <script>
        // Add task 
        const openPopupButton = document.getElementById("add-task-btn");
        const popup = document.getElementById("popup");
        const closePopupButton = document.getElementById("close-popup-button");

        openPopupButton.addEventListener("click", function () {
            popup.style.display = "block";
        });

        closePopupButton.addEventListener("click", function () {
            popup.style.display = "none";
        });

        window.addEventListener("click", function (event) {
            if (event.target === popup) {
                popup.style.display = "none";
            }
        });

        // Search 
        const searchBtn = document.getElementById('pop-up-search-btn');
        const search = document.getElementById('pop-up-search');
        const closepopUp = document.getElementById('search-close');

        searchBtn.addEventListener('click', function () {
            popupsearch.style.display = "block"
        });
        closepopUp.addEventListener('click', function () {
            popupsearch.style.display = "none"
        });
        window.addEventListener('click', function (event) {
            if (event.target == popupsearch) {
                popupsearch.style.display = "none";
            }
        });

        // Today 
        const todayBtn = document.getElementById('today-btn');
        const resultContainer = document.getElementById('result-container');

        todayBtn.addEventListener('click', function () {
            popuptoday.style.display = "block";
        });

        window.addEventListener('click', function (event) {
            if (event.target == popuptoday) {
                popuptoday.style.display = "none";
            }
        });



        // Store data 
        document.getElementById('popup-form').addEventListener('submit', function (event) {
            event.preventDefault();

            const nameInput = document.getElementById('name');
            const name = nameInput.value;
            const formData = {
                name: name,
            };

            const formDataArray = JSON.parse(localStorage.getItem("formDataArray")) || [];
            formDataArray.push(formData);

            localStorage.setItem("formDataArray", JSON.stringify(formDataArray));

            console.log("Form data stored:", formData);
            alert("Form data submitted successfully!");
        });

        // Retrive data

        const formDataArray = JSON.parse(localStorage.getItem("formDataArray")) || [];
        const resultsList = document.getElementById("results-list");

        // Clear any existing content inside the "results-list" ul
        resultsList.innerHTML = "";

        formDataArray.forEach(formData => {
            const name = formData.name;

            // Create a list item for each name
            const listItem = document.createElement("li");
            listItem.style.margin = "2vh";

            // Create a span element to display the name
            const nameElement = document.createElement("span");
            nameElement.textContent = `Name: ${name}`;
            listItem.appendChild(nameElement);

            // Create an "Edit" button
            const editButton = document.createElement("button");
            editButton.textContent = "Edit";
            editButton.addEventListener("click", () => editName(formDataArray, formData, nameElement));
            editButton.classList.add('edit-btn');

            // Create a "Delete" button
            const deleteButton = document.createElement("button");
            deleteButton.textContent = "Delete";
            deleteButton.addEventListener("click", () => deleteName(formDataArray, formData, listItem));
            deleteButton.classList.add('delete-btn');

            // Append the "Edit" and "Delete" buttons to the list item
            listItem.appendChild(editButton);
            listItem.appendChild(deleteButton);

            // Append the list item to the "results-list"
            resultsList.appendChild(listItem);
        });

        function editName(formDataArray, formData, nameElement) {
            // Prompt the user to edit the name
            const newName = prompt("Edit the name:", formData.name);
            if (newName !== null) {
                formData.name = newName;
                nameElement.textContent = `Name: ${newName}`;
                // Update the modified data in localStorage
                localStorage.setItem("formDataArray", JSON.stringify(formDataArray));
            }
        }

        function deleteName(formDataArray, formData, listItem) {
            // Find the index of the data to delete
            const index = formDataArray.indexOf(formData);
            if (index !== -1) {
                formDataArray.splice(index, 1);
                // Remove the list item from the DOM
                listItem.remove();
                // Update the data in localStorage
                localStorage.setItem("formDataArray", JSON.stringify(formDataArray));
            }
        }



    </script>
</body>

</html>
