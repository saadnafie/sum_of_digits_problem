# sum_of_digits_problem
sum_of_digits_problem

<?php
/* --------------------------------
1) Sum of Digits
Write a PHP program to print sum of digits.
Input: 23
Output: 5
-------------------------------- */
Class Digit{

    private int $digit;
    private $digitCount;
    
    public function __construct($digit){
        $this->digit = $digit;
        $this->digitCount = 0;
    }

    public function sumDigit(){
        $sum = 0;
        while($this->digit > 0){
            $this->digitCount =  $this->digitCount + 1;
            $sum = $sum + ($this->digit % 10);
            $this->digit = $this->digit / 10;
        }

        return $sum;
    }

    public function getDigitCount(){
        return $this->digitCount;
    }


}

//$start = microtime(true);
$obj = new Digit(23);
echo "Sum of Digits = ".$obj->sumDigit();
echo " ,Count of Digits = ".$obj->getDigitCount();
//$time_elapsed_secs = microtime(true) - $start;
//echo " ,Time = ".$time_elapsed_secs;
