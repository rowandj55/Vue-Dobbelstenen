<template>
    <ChildComponent @addRoll="addDiceRoll" />
    <table>
        <tr>
            <th>Getal</th>
            <th>Aantal</th>
        </tr>
        <tr>
            <td>1</td>
            <td id="countOne">{{ count[1] }}</td>
        </tr>
        <tr>
            <td>2</td>
            <td id="countTwo">{{ count[2] }}</td>
        </tr>
        <tr>
            <td>3</td>
            <td id="countThree">{{ count[3] }}</td>
        </tr>
        <tr>
            <td>4</td>
            <td id="countFour">{{ count[4] }}</td>
        </tr>
        <tr>
            <td>5</td>
            <td id="countFive">{{ count[5] }}</td>
        </tr>
        <tr>
            <td>6</td>
            <td id="countSix">{{ count[6] }}</td>
        </tr>
    </table>
</template>

<script setup>
import {ref} from 'vue';
import ChildComponent from './components/ChildComponent.vue';

const count = ref({
    1: 0,
    2: 0,
    3: 0,
    4: 0,
    5: 0,
    6: 0,
});

const addDiceRoll = num => {
    count[num]++;
};

// const buttonThrow = document.getElementById('buttonThrow');
// const diceTotalEyes = 6;
// const totalThrows = [
//     document.getElementById('countOne'),
//     document.getElementById('countTwo'),
//     document.getElementById('countThree'),
//     document.getElementById('countFour'),
//     document.getElementById('countFive'),
//     document.getElementById('countSix'),
// ];

// function rollDice() {
//     const count = {
//         1: 0,
//         2: 0,
//         3: 0,
//         4: 0,
//         5: 0,
//         6: 0,
//     };

//     for (let i = 0; i < 8; i++) {
//         let roll = Math.floor(Math.random() * diceTotalEyes + 1);
//         count[roll]++;
//     }

//     for (let i = 0; i < totalThrows.length; i++) {
//         totalThrows[i].textContent = count[i + 1];
//     }
// }

// buttonThrow.addEventListener('click', rollDice);
</script>
