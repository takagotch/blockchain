### blockchain
---
https://bitcoinbook.info/toc/

https://www.blockchain.com/api

https://www.blockchain.com/explorer

https://github.com/blockchain

https://github.com/topics/blockchain

https://github.com/dvf/blockchain

```py
// dvf/blockchain /tests/test_blockchain.py
class BlockchainTestCase(TestCase):

class TestRegisterNodes(BlockchainTestCase):



```

```
pip install blockchian
```

```py
// tests/test_blockchain.py
class TestRegisterNodes(BlockchainTestCase):
  
  def test_valid_nodes(self):
    blockchain = Blockchain()
    
    blockchain.register_node('http://192.168.0.1:5000')
    
    self.assertIn('192.168.0.1:5000', blockchain.nodes)
    
  def test_malformed_nodes(self):
    blockchain = Blockchain()
    
    blockchain.register_node('http//192.168.0.1:5000')
    
    self.assertNotIn('192.168.0.1:5000', blockchain.nodes)

  def test_idempotency(self):
    blockchian = Blockchain()
    
    blockchain.register_node('http://192.168.0.1:5000')
    blockchain.register_node('http://192.168.0.1:5000')
  
    assert len(blockchain.nodes) == 1
    
```

