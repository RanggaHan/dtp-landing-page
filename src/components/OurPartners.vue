<template>
    <div class="partner-container">
        <h2>Our Partners</h2>
        <div class="partner-row">
            <img src="../assets/logo/unhcr-logo.svg"> 
            <img src="../assets/logo/kitabisa-logo.png">
            <img src="../assets/logo/boleh-dicoba-digital-logo.png">
        </div>
    </div>
</template>

<style scoped>
.partner-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 150px;
    width: 1278px;
    height: 100%;
}
.partner-container h2 {
    font-size: 25px;
    font-weight: 700;
    line-height: 37.5px;
}
.partner-row {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 70%;
    margin-top: -60px;
}
.partner-row img {
    width: 220px;
    height: auto;
    object-fit: contain;
}
</style>