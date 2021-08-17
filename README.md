# [Google Clone](https://gooogle-sourav.web.app/) #

## Use the package manager [npm](https://www.npmjs.com/) to install
```
npm install react-router-dom
npm install @material-ui/core
npm install @material-ui/icons
```
## Google Custom Search
```javascript
const UseGoogleSearch = (term) => {

    const [data, setData] = useState(null);

    useEffect(() => {
        const fetchData = async () => {
            fetch(`https://www.googleapis.com/customsearch/v1?key=${API_KEY}&cx=${CONTEXT_KEY}&q=${term}`)
                .then(response => response.json())
                .then(result => {
                    setData(result)
                })
        }
        fetchData().then(res => {
            console.log(res);
        }).catch(error => {
            console.log(error);
        });
    }, [term]);

    return {data};
};

This website uses Material-UI which eases the styling part. Use your own API key to activate the search engine and feel free to clone the repository and personalize the project.
