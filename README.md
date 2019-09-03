# Stock challenge
Reverse engineering stock data in order to make a profitable algorithm.

### Dependencies
Using python 3.7.3
``` 
pip install pandas seaborn jupyter
```

### Notes
- May be worth inspecting data beforehand.
- Data can be read in via pandas `.read_csv()`.
- Going with strategy of making as much trades as possible. May include variable offset to improve efficiency.
- This will involve going through the dataset in increments of 30 (minimum cooldown period) and cherry picking profitable windows.
- This process will heavily rely on manipulating the index in a recursive fashion (while loop) and conditionally updating it based on future indices and prices.
- Results will be stored in a list of python dictionaries. From that total trades, profit and lineage can be traced.

### Limitations
- May be seen as a naive approach, however is a minimum viable solution.
- No heavy type/null validation or error catching set in place, assumes csvs will come in the same format every time. That is headers will remain constant, no nulls will be present. Types will remain consistent.
- Takes a non mathetical approach, no statistical methods were used.

