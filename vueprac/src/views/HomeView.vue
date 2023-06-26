 <template>
  <div>
    <h1>Home</h1>
    <div id="display"></div>
 
  </div>
 </template>
 
 <script>


  async function getData(){
      const data = await fetch('https://maarij-camroodien.github.io/json-server/index.json')
      const formatData = await data.json()

      console.log(formatData);
  
      extractedData = formatData.cars
  
      const display = document.querySelector('#display')
  
      extractedData.forEach(cars =>{
      display.innerHTML += `
      <div class="card">
          <img src="${cars.image}" style="width: 18rem" alt="">
          <div class="card-body">
            <h3 class="card-title">${cars.name}</h3>
            <p class="card-text">${cars.model}</p>
            <p class="card-text">${cars.price}</p>
          </div>
        </div>
    `
  })
  }
  
    getData()
 </script>
 
 <style>
 #display {
  /* display: flex;
  justify-content: center;
  align-content: center; */
  text-align: center;
 }
 
 .card {
  margin: 1rem;
 }
 
 h1 {
  text-align: center;
 }
 
 </style>
