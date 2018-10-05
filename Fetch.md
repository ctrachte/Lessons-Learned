## The below code is an example of a fetch API call I made recently in React.
- taking notes here to reference later.

```
fetch("coolURL.api.com", {
  headers: {
      'Access-Control-Request-Headers': '*'
    }
})
  .then(res => res.json())
  .then(

    (result) => {
      this.setState({
        isLoaded: true,
        items: result.results
      });
    },
    // Note: it's important to handle errors here
    // instead of a catch() block so that we don't swallow
    // exceptions from actual bugs in components.
    (error) => {
      console.log(error);
      this.setState({
        isLoaded: true,
        error
      });
    }
  )
```
