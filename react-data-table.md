layout: page
title: "react-data-table-componant"
permalink: /tutorial/react-data-table

## React-Data-Table-Component Tutorial

welcome to my frirst ever tutorial that I have written :-/. So if you have come this far then you have already got the jist of what I have been up to.

### learning to use the component

the story book on this repository is pretty good, but as I am still learning there was things I struggled to get my head around and spent too long (in my opinion to figure out)
but hey thats just the way I do things.

I was getting data from an api that we created, I am quite familiar with the api and I know what data comes out of it. My first hurdle was how do I get my data to display in my new table.
turns out it is easier then I thought...

firstly I used useEffect() and the first call was to use Axios to get my data, looked like this

```javascript
useEffect(()=> {
        axios.get(getUrl).then(resp =>{
            const {results = []} = resp.data;
            setData(results);
            setLoading(false);
            setHightlighting(true);
            setFilterText('');
        }).catch(() => {
            setLoading(false);
            setData(null);
            setFilterText('');
        });
    },[]);
    ```
