months,
.years {
    padding: 2%;
    margin: 2%;
    /* position: relative; */
    font-family: 'Times New Roman';
    font-size: 150%;
}

.input {
    padding: 1% 1%;
    font-family: 'Times New Roman';
    font-size: 150%;
    width: 15%;
}

.button {
    padding: 1% 1%;
    font-family: 'Times New Roman';
    font-size: 150%;
    width: 10%;
}

ul {
    list-style-type: none;
}

.weekdays {
    margin: 0%;
    padding: 1% 0%;
    border: 1px solid;
}

.weekdays li {
    display: inline-block;
    width: 13%;
    text-align: center;
    padding: 1% 0%;
    font-size: 20px;
}

.days {
    padding: 1% 0%;
    margin: 0;
    border: 1px solid;
}

.days li {
    list-style-type: none;
    display: inline-block;
    width: 13%;
    text-align: center;
    margin-bottom: 5px;
    font-size: 20px;
    padding: 1% 0%;
}
</style> Select Month January February March April May June July Augest September October November December Select Year 1999 2000 2001 2002 2003 2004 2005 2006 2007 2008 2009 2010 2011 2012 2013 2014 2015 2016 2017 2018 2019 2020 2021 2022 MON TUE WED THR FRI SAT SUN
Please select "Month" or "Year" to display days
    </div>
    <br><br>
    <div>
        <form>
            <input type="number" class="input" id="enteredDay" placeholder="Enter any day" onchange="monthsDays()"
                min="1" max="31"></input>
            <button type="button" class="button" onclick="monthsDays()">Enter</button>
        </form>
    </div>
</div>
<script> var enteredDay = document.getElementsByTagName("input")[0].value; var getYear = () => document.getElementById("years").value; var getDays = () => { var selectedMonth = document.getElementById("months").value; var days = 31; if ((selectedMonth == 'apr') || (selectedMonth == 'jun') || (selectedMonth == 'sep') || (selectedMonth == 'nov')) { return days = 30; } else if (selectedMonth == "feb") { let year = getYear(); const leap = new Date(year, 1, 29).getDate() === 29; if (leap) { return days = 29; } else { return days = 28; } } else { return days = 31; } } var daysOfMonth = () => { let days = getDays(); var str = '
'.repeat(3); for (let day = 1; day <= days; day++) { if (document.getElementById("enteredDay").value == day) { if ("green" == document.getElementById("enteredDay").style.backgroundColor) { str = str + (`
${day}
`); } else { str = str + (`
${day}
`); } } else { str = str + (`
${day}
`); } [ ] } return str; } var monthsDays = () => document.getElementById("days-of-month").innerHTML = daysOfMonth(); </script>
—


