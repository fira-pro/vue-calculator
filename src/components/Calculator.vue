<script setup>

const basicCalRows = {
    row1: {
        0: { value: 0, id: "num-0", class: "btn num" },
        decpoint: { value: '.', id: 'decimal-point', class: 'btn' },
        equal: { value: '=', id: 'equality', class: 'btn ' },
        add: { value: '+', id: 'addition', class: 'btn op' },
    },
    row2: {
        1: { value: 1, id: "num-1", class: "btn num" },
        2: { value: 2, id: "num-2", class: "btn num" },
        3: { value: 3, id: "num-3", class: "btn num" },
        sub: { value: '-', id: 'subtraction', class: 'btn op' },
    },
    row3: {
        4: { value: 4, id: "num-4", class: "btn num" },
        5: { value: 5, id: "num-5", class: "btn num" },
        6: { value: 6, id: "num-6", class: "btn num" },
        mult: { value: '×', id: 'multiplication', class: 'btn op' },
    },
    row4: {
        7: { value: 7, id: "num-7", class: "btn num" },
        8: { value: 8, id: "num-8", class: "btn num" },
        9: { value: 9, id: "num-9", class: "btn num" },
        div: { value: '÷', id: 'division', class: 'btn op' },
    },
    row5: {
        openbrkt: { value: '(', id: 'open-bracket', class: 'btn' },
        closebrkt: { value: ')', id: 'open-bracket', class: 'btn' },
        perc: { value: '%', id: 'percentage', class: 'btn op' },
        allClear: { value: 'AC', id: 'all-clear', class: 'btn' }
    }
}

const revBasicCalRows = Object.keys(basicCalRows).reverse();

</script>

<template>
    <div id="calc-container">
        <div id="calc-btns">
            <table>
                <tr v-for="row in Object.keys(basicCalRows).reverse()" :key="row">
                    <td v-for="btn in basicCalRows[row]" :key="btn.id" :class="btn.class" :id="btn.id">
                        {{ btn.value }}
                    </td>
                </tr>
            </table>
        </div>
        <div id="calc-screen">
        </div>

    </div>
</template>


<style scoped>
#calc-container {
margin: 10px 30px 10px 30px;
border: 2px solid red;
}

#calc-btns {
margin: auto;
border: solid blueviolet;
}

#calc-btns table {
    width: 100%;
    min-width: 250px;
    max-width: 400px;
    border-spacing: 10px;
    border: 2px solid green;
    margin:auto;
}

.btn {
    border-bottom: 4px solid rgb(73, 57, 57);
    border-right: 4px solid rgb(157, 163, 170);
    border-radius: 5px;
    width: 24%;
    text-align: center;
    font-size: 1.5em;
    background:rgb(172, 175, 177);
    user-select: none;
    padding: 3px;
    font-weight: light;
    color:rgb(13, 13, 13);
   

    

}

.btn:active {
    border: none;
}


</style>