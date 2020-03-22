# Almabase

## Heroku

```
https://almabase-github-gaurisankarj.herokuapp.com/:organization?m=<number_of_repositories>&n=<number_of_committees>
```

## Local, PORT=3000

```
npm start
```

### API

> Input : Organization Name, Number of top Repositories by fork count (m), Number of top Committees by commit count (n)

> Output : Top m Repositories with top n committees and their commit counts

* **URL**
  
  ```
  /:organization?m=<number_of_repositories>&n=<number_of_committees>
  ```

* **Method:**

  ```
  GET
  ```

* **URL Params**
  
  ```
  /:organization
  ```

* **Query Params**
  
  ```
  ?m=<number_of_repositories>&n=<number_of_committees>
  ```

* **Success Response:**
  * ***Code:*** 200
* **Error Response:**
  * ***Code:*** 404 RESOURCE NOT FOUND
  * ***Code:*** 400 BAD REQUEST
* **Sample Call:**
  
  ```
  curl https://almabase-github-gaurisankarj.herokuapp.com/google?m=2&n=2
  ```

* **Sample Response:**
  ```
    {
        dagger: [
                    {
                    name: "Chris Povirk",
                    count: 16
                    },
                    {
                        name: "Kurt Alfred Kluever",
                        count: 7
                    }
                ],
        traceur-compiler: [
                    {
                    name: "Erik Arvidsson",
                    count: 24
                    },
                    {
                    name: "johnjbarton",
                    count: 4
                    }
                ]
    }
  ```