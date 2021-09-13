<template>
 <span>Привет, меня зовут Макс! Я хочу  Верстать :)</span>
    <div id="cursor"></div>
    <div id="aura"></div>
</template>

<script>
export default {
  name: 'FolderView',
  props: {
    name: String,
    folders:Array,
    files:Array
  }
}
  document.addEventListener('mousemove', function(e) {
    var cursor = document.getElementById('cursor');
    var aura = document.getElementById('aura');
    var x = e.clientX;
    var y = e.clientY;
    cursor.style.left = x + 'px';
    cursor.style.top = y + 'px';
    aura.style.left = x + 'px';
    aura.style.top = y + 'px';
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
body {
    margin: 0%;
    padding: 0%;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    overflow: hidden;
    cursor: none;
}

#cursor {
    position: absolute;
    width: 10px;
    height: 10px;
    background: rgb(110, 110, 110);
    box-sizing: border-box;
    transition: 0.1s;
    transform: translate(-50%, -50%);
    border-radius: 50%;
    pointer-events: none;
}

#aura {
    position: absolute;
    width: 35px;
    height: 35px;
    border: 2px solid black;
    box-sizing: border-box;
    transition: 0.2s;
    transform: translate(-50%, -50%);
    border-radius: 50%;
    pointer-events: none;
}

span {
    width: auto;
    height: 30px;
    transition: 1s;
}

span:hover~#aura {
    width: 50px;
    height: 50px;
    border: 2px dashed black;
}

span:hover~#cursor {
    background: rgba(110, 110, 110, 0);
}

span:hover {
    width: auto;
    transition: 1s;
    font-size: 24px;
    color: rgb(255, 50, 50);
}</style>
