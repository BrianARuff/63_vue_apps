<template>
   <div>
      <h4>{{ quote.text }}</h4>
      <p>{{ quote.author }}</p>
      <button @click="generateQuote">Generate Quote</button>
   </div>
</template>

<script>

const quotes = [
   {
      text: 'The best way to learn anything is to try and fail without trying.',
      author: 'Albert Einstein'
   },
   {
      text: 'The only way to do good is to do enough.',
      author: 'Aristotle'
   },
   {
      text: 'The only way to do good is to do enough.',
      author: 'Twiggy'
   },
   {
      text: "Mayne I'm the one who is the schizophrenic psycho",
      author: 'James Pain'
   },
   {
      text: "I'm a good person, I just don't know what to do with myself",
      author: 'Tina Fey'
   },
   {
      text: "No you aren't, that is just an exuse",
      author: 'Brian Ruff'
   },
   {
      text: 'Oh okay, maybe you are, what do I know, not much...',
      author: 'Brian Ruff'
   },
   {
      text: "I'm not sure what you mean, I'm just a person",
      author: 'VS Code Co-pilot'
   }
];
export default {
   data(){
      return {
         quote: quotes[Math.floor(Math.random() * quotes.length)]
      };
   },
   methods: {
      generateQuote() {
         this.quote = quotes[Math.floor(Math.random() * quotes.length)];
      }
   }
};
</script>