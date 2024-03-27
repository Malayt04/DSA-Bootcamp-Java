# [Video link](https://youtu.be/fzip9Aml6og)

## Problems

## Easy
- [Add Binary](https://leetcode.com/problems/add-binary/) // Have to do once again
- [Single Number](https://leetcode.com/problems/single-number/)  Done (Xor operation on alll the elements of the array this will return the unique element)
- [Reverse Bits](https://leetcode.com/problems/reverse-bits/)  remember for(i=0; i<32; i++){rev=<<1 rev|=(n&1) n=>>1}
- [Number of 1 Bits](https://leetcode.com/problems/number-of-1-bits/) Done(right shift n and take & with 1)
- [Counting Bits](https://leetcode.com/problems/counting-bits/) Done, Same as above
- [Binary Watch](https://leetcode.com/problems/binary-watch/)  for (int h=0; h<12; h++)
        for (int m=0; m<60; m++)
            if (Integer.bitCount(h * 64 + m) == num)
                times.add(String.format("%d:%02d", h, m));
    return times;  ***One more time
- [Hamming Distance](https://leetcode.com/problems/hamming-distance/) return number of set bits present in x^y
- [Number Complement](https://leetcode.com/problems/number-complement/) Done
- [Set Mismatch](https://leetcode.com/problems/set-mismatch/) Confused about testcases
- [Binary Number with Alternating Bits](https://leetcode.com/problems/binary-number-with-alternating-bits/) Done
- [Prime Number of Set Bits in Binary Representation](https://leetcode.com/problems/prime-number-of-set-bits-in-binary-representation/) Done
- [Binary Gap](https://leetcode.com/problems/binary-gap/) Done
- [Number of Steps to Reduce a Number to Zero](https://leetcode.com/problems/number-of-steps-to-reduce-a-number-to-zero/) Done
- [Sort Integers by The Number of 1 Bits](https://leetcode.com/problems/sort-integers-by-the-number-of-1-bits/) Done
- [XOR Operation in an Array](https://leetcode.com/problems/xor-operation-in-an-array/) Done
- [Count the Number of Consistent Strings](https://leetcode.com/problems/count-the-number-of-consistent-strings/)
- [Decode XORed Array](https://leetcode.com/problems/decode-xored-array/)
- [Sum of All Subset XOR Totals](https://leetcode.com/problems/sum-of-all-subset-xor-totals/)
- [Longest Nice Substring](https://leetcode.com/problems/longest-nice-substring/)

## Medium

###Note:  Many questions follow the pattern of counting number of set bits 


- [Subsets](https://leetcode.com/problems/subsets/)<br>
```
for(int i=0; i<subsetLength; i++){
            List<Integer> subset = new ArrayList<>();
            for(int j=0; j<n; j++){
                if((int)(i&(1<<j))!=0){
                    subset.add(nums[j]);
                }
            }
            ans.add(subset);
        }
```
- [Subsets II](https://leetcode.com/problems/subsets-ii/)
  Same as Above just check if the subset is already present in the answer and maniplate accordingly.
- [Single Number II](https://leetcode.com/problems/single-number-ii/)
  O(n^2)
  ```
  for (int num : nums) {
        for (int i = 0; i < 32; i++) {
            if ((num & (1 << i)) != 0) {
                counts[i]++;
            }
        }
    }
    for (int i = 0; i < 32; i++) {
        result |= (counts[i] % 3) << i;
    }
  ```
  O(n)
  ```
   for (int num : nums) {
        ones = (ones ^ num) & ~twos;
        twos = (twos ^ num) & ~ones;
    }
  ```
  
- [Divide Two Integers](https://leetcode.com/problems/divide-two-integers/)
- [Gray Code](https://leetcode.com/problems/gray-code/)
- [Repeated DNA Sequences](https://leetcode.com/problems/repeated-dna-sequences/)

## Hard
- [Minimum Number of Flips to onvert Binary Matrix to zero matrix](https://leetcode.com/problems/minimum-number-of-flips-to-convert-binary-matrix-to-zero-matrix/)
- [Minimum cost to connect two group of points](https://leetcode.com/problems/minimum-cost-to-connect-two-groups-of-points/)
- [Find XOR Sum of All Pairs Bitwise AND](https://leetcode.com/problems/find-xor-sum-of-all-pairs-bitwise-and/)

# Additionally
- Click on [*Show problem tags*](https://leetcode.com/tag/bit-manipulation/) and do the questions that contains tags of topics we have covered so far.
