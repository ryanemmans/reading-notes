# CLASS 1 NOTES - Node Ecosystem, TDD, CI/CD

***1. Describe (in plain English) what `Array.map()` does***

- `Array.map()` iterates through an array and calls a provided function for each element in that array, in order. It then constructs a new array from the results of said function call.

***2. Describe (in plain English) what `Array.reduce()` does***

- Similar to `.map`, `Array.reduce()` iterates through an array. It runs a callback on every element in an array and returns something new based on an `accumulator` parameter. It also takes in a value and an index as well as the initial value of the accumulator. The original array is not modified.
- A common use case for `.reduce` is to return the *sum* of all elements in an array.

***3. Provide code snippets showing how to use `superagent()` to fetch data from a URL and log the result***

- With normal Promise `.then()` syntax:

    ```js
    let getCharacters = () => {
      superagent.get('https://swapi.dev/api/people')
      .then((data) => {
        let results = data.body.results.map(char => {
          return ({ [char.name]: char.url })
        })
        console.log(results);
      })
        .catch(err => console.error(err));
    };

    getCharacters();
    ```

- Again with `async` / `await` syntax:

    ```js
    async function retrieveData(city) {
      try {
      let data = await superagent.get(`https://geocode.xyz/${city}?json=1`);
      console.log(`${data.body.standard.city}: Lat ${data.body.latt}, Lon ${data.body.longt}`);
      } catch(err) {
        console.error(err);
      }
    }

    retrieveData('Seattle');
    ```

***4. Explain promises as though you were mentoring a Code 301 level student***

- Promises can handle Asynchronous actions in JavaScript. Similar to callbacks, promises enable you to execute code and move on, allowing that code to take as long as needed to run. Promises tend to read more inline than callbacks.
- A promise tells JavaScript to run code. Once that code has completed, the promise can then handle the data.
- An asynchronous promise is considered any function that simply “returns an instance of a promise.” They can either work or fail, or in other words `resolve` or `reject`.
- Promises can run independently (out of sequence), or also *chained* to run in sequence.

***5. Are all callback functions considered to be Asynchronous? Why or Why Not?***

- Not all callback functions are considered Asynchronous. Synchronous callbacks would be considered 'standard' (however, less practical) and are executed immediately, whereas Asynchronous callbacks can be used to continue code execution after an operation has run.

- - -

Sources:

- [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Code Fellows GitHub - Callbacks](https://codefellows.github.io/code-401-javascript-guide/curriculum/prework/callbacks/)
- [Code Fellows GitHub - Promises](https://codefellows.github.io/code-401-javascript-guide/curriculum/prework/promises/)
- [Code Fellows GitHub - Async/Await](https://codefellows.github.io/code-401-javascript-guide/curriculum/prework/async-await/)

[back](../README.md)
