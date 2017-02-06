//The common solution to this problem was to use a loop to manually go through the candle burning logic.
//It is much more efficient to use an algorythm which has a constant time complexity rather than the linear complexity
//that a loop creates.

//Overview: 
    //The idea is that a certain number of burned candles can be recycled into new candles to be burned again. 
    //The output gives the number of candles burned given a certain starting number and the number of used 
    //candles required to make a new one.
    
//Limits and Consideration
    //The candles function is constrained to always output >= 1.
    //The inputs are constrained to prevent division by 0.
    //Since division is done with ulong the number is effectively rounded down. 
    //This same priniple applies to all non-decimal number data types.
    //The only effective ceiling for inputs is the max value of ulong 18,446,744,073,709,551,615.
    //At max load (candlesNumber = 18,446,744,073,709,551,615 and makeNew = 2) execution is under 1 milisecond.
    //Data type can be changed to the appropriately sized data type so long as it is not a decimal data type(double, float, or decimal).
    //These data types will cause a rounding error and report fractional candles.

int candles(ulong candlesNumber, ulong makeNew) {
    if(candlesNumber >=1 && makeNew >= 2)
    {
        return candlesNumber +((candlesNumber-1)/(makeNew-1));
    }
    else return -1;
}
