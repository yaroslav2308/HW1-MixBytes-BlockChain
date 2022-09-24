# HW1-MixBytes-BlockChain

Git diff of first task:
```
function submitTransaction(address destination, uint value, bytes data)
     public
     returns (uint transactionId)
 {
+    require(value <= 66 ether, "it is not allowed to send more than 66 ether in one transaction");
     transactionId = addTransaction(destination, value, data);
     confirmTransaction(transactionId);
 }
```
 
