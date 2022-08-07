# fixermake.github.io
Fixer Make Website

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
    <title>Online exam</title>
    <style>
        html,body {
            font-family: Helvetica Neue,Helvetica,Arial,sans-serif;
            -webkit-font-smoothing: antialiased;
        }   
        .d-none{
            display:none;
        }
        nav#nevigation{
            position:fixed;
            top: 0;
            left: 0;
            z-index: 1000;
            width:100%;
            height: auto;
            background-color:#fff;
            box-shadow: 0 1px 5px 0 rgb(0 0 0 / 10%);
        }
        nav#nevigation > div.container{
            position: relative;
            display: flex;
            flex-direction: row;
            align-items: center;
            background: #fdfdfd;
            line-height: 60px;
            width:100%;
        }
        nav#nevigation > div.container > div.icon{
            display: flex;
            align-items: center;
            font-size: 1.25rem;
            margin-left: 2%;
            margin-right: 2%;
        }
        nav#nevigation > div.container > div.icon > span.icon{
            width: 35px;
            height: 35px;
        }
        nav#nevigation > div.container > div.icon > span.name{
            margin-left: 15px;
        }
        nav#nevigation > div.container > div.page{
            display: flex;
        }
        nav#nevigation > div.container > div.page > div{
            display: flex;
            cursor: pointer;
            align-items: center;
            font-size: 0.9375rem;
            text-transform: capitalize;
            margin: 0;
            padding: 0 20px;
            color: #515a6e;
            border-bottom: 2px solid #fff;
        }
        nav#nevigation > div.container > div.page > div.active,
        nav#nevigation > div.container > div.page > div:hover{
            color: #2d8cf0;
            border-bottom: 2px solid #2d8cf0;
        }
        nav#nevigation > div.container > div.page > div > span{
            display: flex;
        }
        nav#nevigation > div.container > div.page > div > span.icon > svg{
            margin-right: 9px;
            width: 15px;
            height:15px;
        }
        nav#nevigation > div.container > div.authentication{
            margin-left: auto;
            margin-right: 10px;
        }
        nav#nevigation > div.container > div.authentication > div.login-register > button{
            height:32px;
            padding: 0 15px;
            cursor: pointer;
            font-size: 0.875rem;
            border-radius: 32px;
            vertical-align:middle;
            font-weight: 400;
            text-align: center;
            transition: color .2s linear,background-color .2s linear,border .2s linear,box-shadow .2s linear,-webkit-box-shadow .2s linear;
            color: #515a6e;
            background-color: #fff;
            border: 1px solid #dcdee2;
            text-transform: capitalize;
        }
        nav#nevigation > div.container > div.authentication > div.login-register > button:hover,
        nav#nevigation > div.container > div.authentication > div.profile > button.name:hover{
            color: #57a3f3;
            background-color: #fff;
            border-color: #57a3f3;
        }
        nav#nevigation > div.container > div.authentication > div.profile{
            position:relative;
            margin-right: 30px;
        }
        nav#nevigation > div.container > div.authentication > div.profile > button.name{
            min-width: 100px;
            max-width: 100px;
            display: flex;
            align-items:center;
            border: none;
            background-color:#fff;
            transition: color .2s linear,background-color .2s linear,border .2s linear,box-shadow .2s linear,-webkit-box-shadow .2s linear;
            padding:0 15px;
            line-height: 1.5;
            font-size: 1.125rem;
        }
        nav#nevigation > div.container > div.authentication > div.profile > button.name > svg{
            width: 14px;
            height:14px;
            margin-left: 7px;
        }
        nav#nevigation > div.container > div.authentication > div.profile > div.container{
            position: absolute;
            z-index: 900;
            top: 60px;
            left: 0px;
            min-width: 100px;
        }
        nav#nevigation > div.container > div.authentication > div.profile > div.container > ul.dropdown{
            padding: 0;
            margin:0;
            width:100%;
            height: 100%;
            overflow: hidden;
            margin: 5px 0;
            padding: 5px 0;
            background-color: #fff;
            border-radius: 4px;
            box-shadow: 0 1px 6px rgb(0 0 0 / 20%);
            list-style: none;
            text-transform: capitalize;
        }
        nav#nevigation > div.container > div.authentication > div.profile > div.container > ul.dropdown > li.row{
            display: flex;
            align-items: center;
            justify-content: center;
            line-height: normal;
            padding: 7px 16px;
            cursor: pointer;
            color: #515a6e;
            font-size: 0.875rem!important;
            -webkit-transition: background .2s ease-in-out;
            transition: background .2s ease-in-out;
        }
        nav#nevigation > div.container > div.authentication > div.profile > div.container > ul.dropdown > li.row:hover{
            background-color:#f3f3f3;
        }
        nav#nevigation > div.container > div.authentication > div.profile > div.container > ul.dropdown.deactive{
            height: 0;
            padding-top: 0px;
            padding-bottom: 0px;
        }
        nav#nevigation > div.container > div.authentication > div.profile > div.container > ul.dropdown > li.row:not(:first-child){
            margin-top: 5px;
            border-top: 1px solid #e8eaec;
        }
        nav#nevigation > div.container > div.authentication > div.profile > button.name:focus{
            
        }

    </style>
</head>
<body>
    <nav id="nevigation">
        <div class="container">
            <div class="icon">
                <span class="icon"><img src="C:\Users\hilwo\OneDrive\Downloads\download (2).svg" alt="Not found"></span>
                <span class="name">Icon is hear</span>
            </div>
            <div class="page">
                <div class="home active">
                    <span class="icon">
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" viewBox="0 0 16 16"><path d="M6.5 14.5v-3.505c0-.245.25-.495.5-.495h2c.25 0 .5.25.5.5v3.5a.5.5 0 0 0 .5.5h4a.5.5 0 0 0 .5-.5v-7a.5.5 0 0 0-.146-.354L13 5.793V2.5a.5.5 0 0 0-.5-.5h-1a.5.5 0 0 0-.5.5v1.293L8.354 1.146a.5.5 0 0 0-.708 0l-6 6A.5.5 0 0 0 1.5 7.5v7a.5.5 0 0 0 .5.5h4a.5.5 0 0 0 .5-.5z"/></svg>
                    </span>
                    <span class="name">home</span>
                </div>
                <div class="help">
                    <span class="icon">
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" viewBox="0 0 16 16"><path d="M8 16A8 8 0 1 0 8 0a8 8 0 0 0 0 16zm.93-9.412-1 4.705c-.07.34.029.533.304.533.194 0 .487-.07.686-.246l-.088.416c-.287.346-.92.598-1.465.598-.703 0-1.002-.422-.808-1.319l.738-3.468c.064-.293.006-.399-.287-.47l-.451-.081.082-.381 2.29-.287zM8 5.5a1 1 0 1 1 0-2 1 1 0 0 1 0 2z"/></svg>
                    </span>
                    <span class="name">help</span>
                </div>
                <div class="schedule">
                    <span class="icon">
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" viewBox="0 0 16 16"><path d="M14 0H2a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2zM1 3.857C1 3.384 1.448 3 2 3h12c.552 0 1 .384 1 .857v10.286c0 .473-.448.857-1 .857H2c-.552 0-1-.384-1-.857V3.857z"/><path d="M6.5 7a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm-9 3a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm-9 3a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"/></svg>
                    </span>
                    <span class="name">schedule</span>
                </div>
                <div class="profile">
                    <span class="icon">
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"  viewBox="0 0 16 16"><path d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H3zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/></svg>
                    </span>
                    <span class="name">profile</span>
                </div>
            </div>
            <div class="authentication">
                <div class="login-register d-none">
                    <button class="login">login</button>
                    <button class="register">register</button>
                </div>
                <div class="profile">
                    <button class="name">
                        <span>name</span>
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" viewBox="0 0 16 16"><path d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"/></svg>
                    </button>
                    <div class="container">
                        <ul class="dropdown deactive">
                            <li class="row">settings</li>
                            <li class="row">logout</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </nav>
    <script>
        $(document).ready(function(){
            $("nav#nevigation > div.container > div.authentication > div.profile > button.name").focus(function(){
                $("nav#nevigation > div.container > div.authentication > div.profile > div.container > ul.dropdown").removeClass("deactive")
            })
            $("nav#nevigation > div.container > div.authentication > div.profile > button.name").focusout(function(){
                $("nav#nevigation > div.container > div.authentication > div.profile > div.container > ul.dropdown").addClass("deactive")
            })
        })
    </script>
</body>
</html>
