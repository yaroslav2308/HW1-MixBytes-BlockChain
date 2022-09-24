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
Git diff of second task:
```
function _beforeTokenTransfer(address from, address to, uint256 amount) internal virtual 
{ 
+    require((block.timestamp / 86400 + 4) % 7 != 5, "it is not allowed to transfer token on a Saturday");
}
```
Git diff of third task:
```
function() external payable {
+   require(msg.data.length != 0, "cannot send ether without additional message/data");
   if (msg.value > 0) {
       emit Deposit(msg.sender, msg.value);
       m_totalDividends = m_totalDividends.add(msg.value);
   }
}
```
 
