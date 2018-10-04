# design
```
readTextFile => parseInt => square => writeTextFIle
```

```
IBox: {
	postion: {x: , y: }
	id: 
}
```
csvReader {
	uri: file:///tmp/text.txt
	inferHeaders:
	inferSchema:
	schema: []

	slotes:
		in : [{
			type: dataframe
			id : "uid"
		}]
}
```
tranformer {
	id: transformerId
	slotes:
		in: {
			type: dataframe
			id : "uid"
		}
		out: {
			type: dataframe
			id : "uid"
		}
		modifiers: []
}
```
```
filter {
	id: transformerId
	slotes:
		in: {
			type: dataframe
			id : "uid"
		}
		out: {
			type: dataframe
			id : "uid"
		}
		modifiers: []
}
```

fun Box.execute(boxContext, outConnections, InConnections): ExecStatus {
	/*

	*/
	params = boxContext.getParams()
	operants = InConnections.get()
	result = do_operation(operants, params)
	OutConnections.put(Result)
	return ExecStatus()
}
