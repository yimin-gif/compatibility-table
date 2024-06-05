<html>
<head>
    <title>Compatibility Table</title>
    <style>
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 8px;
        }
        th {
            background-color: #f2f2f2;
        }
    </style>
    <script>
        function filterTable() {
            var input, filter, table, tr, td, i, j, txtValue;
            input = document.getElementById("searchInput");
            filter = input.value.toUpperCase();
            table = document.getElementById("compatibilityTable");
            tr = table.getElementsByTagName("tr");

            for (i = 1; i < tr.length; i++) {
                tr[i].style.display = "none";
                td = tr[i].getElementsByTagName("td");
                for (j = 0; j < td.length; j++) {
                    if (td[j]) {
                        txtValue = td[j].textContent || td[j].innerText;
                        if (txtValue.toUpperCase().indexOf(filter) > -1) {
                            tr[i].style.display = "";
                            break;
                        }
                    }
                }
            }
        }
    </script>
</head>
<body>

<h2>Compatibility Table</h2>
<input type="text" id="searchInput" onkeyup="filterTable()" placeholder="Search for models..">

<table id="compatibilityTable">
    <tr>
        <th>Year</th>
        <th>Make</th>
        <th>Model</th>
        <th>Trim</th>
        <th>Engine</th>
        <th>Notes</th>
    </tr>
    <tr>
        <td>2023</td>
        <td>Honda</td>
        <td>Odyssey</td>
        <td>EX-L Mini Passenger Van 4-Door</td>
        <td>3.5L 3471CC V6 GAS SOHC Naturally Aspirated</td>
        <td></td>
    </tr>
    <tr>
        <td>2023</td>
        <td>Honda</td>
        <td>Odyssey</td>
        <td>EX Mini Passenger Van 4-Door</td>
        <td>3.5L 3471CC V6 GAS SOHC Naturally Aspirated</td>
        <td></td>
    </tr>
    <tr>
        <td>2023</td>
        <td>Honda</td>
        <td>Odyssey</td>
        <td>Elite Mini Passenger Van 4-Door</td>
        <td>3.5L 3471CC V6 GAS SOHC Naturally Aspirated</td>
        <td></td>
    </tr>
    <!-- 继续添加更多行 -->
</table>

</body>
</html>
