## 📜 react-dummytext
input에서 선택한 문단 수에 따라 더미텍스트 나타내기
```javascript
const [count, setCount] = useState(0)
const [text, setText] = useState([])

const handleSubmit = (e) => {
  e.preventDefault()
  let amount = parseInt(count)// input에 선택된 count가 문자타입이므로 숫자로 변환
  if(count <= 0){
    amount = 1
  }
  if(count > data.length - 1){
    amount = data.length
  }
  setText(data.slice(0, amount))
}

//폼 부분 
<form className="lorem-form" onSubmit={handleSubmit}>
  <label htmlFor="amount">
    paragraphs:
  </label>
  <input type="number" name="amount" id="amount" value={count}
  onChange={(e) => setCount(e.target.value)}
  />
  <button type="submit" className="btn">generate</button>
</form>
<article className="lorem-text">
  <p>
    {
      text.map((item, index) => {
        return <p key={index}>{item}</p>
      })
    }
  </p>
</article>
```

<참고>
Coding Addict
