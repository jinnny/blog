---
title: "[React] Smart Component vs Dumb Component"
date: 2019-01-04 18:00:00 -0400
categories: React study
---

Smart Component vs Dumb Component
=============

Nomad Corder 사이트에서 React 공부를 시작했습니다.

어렵기에 공부했던 내용들을 정리합니다.

Smart Component 와 Dumb Component 정리를 합니다.

Smart 는 class Component를 의미하고,  Dumb 는 functional Component를 의미합니다.


코드
----
```
Smart Component

class Movie extends Component{
    static propTypes = {
        title: PropTypes.string.isRequired,
        poster: PropTypes.string.isRequired
    }
    render() {
        return (
            <article>
                <MoviePoster poster={this.props.poster}/>
                <h1>{this.props.title}</h1>
            </article>
        )
    }
}

class MoviePoster extends Component{
    static propTypes = {
        poster: PropTypes.string.isRequired
    }
    render() {
        return(
            <img src={this.props.poster} alt="1" /> 
        )
    }
}
```
보시다시피 Smart Component는 this를 사용해야합니다.
그리고 state를 이용해 업데이트가 가능합니다.

동작하는 과정은 아래와 같습니다.

```
Render의 경우, componentWillMount() -> render() -> componentDidMount()
Update의 경우, componentWillReceiveProps() -> shouldComponentUpdate() -> componentWillUpdate() -> render() -> componentDidUpdate()
```


그에 반해 Dumb Component는 this가 불필요하고, 비교적 간단하지만, state가 없기 때문에 업데이트가 불가능합니다.
React 의 멋진 기능을 사용할 수 없기때문에..아주 간단한 작업을 할때는 사용하셔도 무방합니다.

```
function Movie({title,poster}){
    return (
        <article>
            <MoviePoster poster={poster}/>
            <h1>{title}</h1>
        </article>
    )
}
function MoviePoster({poster}){
    return (
        <img src={poster} alt="1" /> 
    )
}

Movie.prototypes = {
    title: PropTypes.string.isRequired,
    poster: PropTypes.string.isRequired
}

MoviePoster.prototypes = {
    poster: PropTypes.string.isRequired
}

```




참고 URL
-------
[Nomad Coders ReactJS로 웹 서비스 만들기](https://academy.nomadcoders.co/courses/216871/lectures/3368679)
