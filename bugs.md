* hasattr(dict, key) is wrong. We can only use "key" grammar in dict.

* torch tensor copy_ method requires the src and dst shape to be the same or can be broadcasted. Because of the broadcast, a[:0].copy_(b[:1]) and a[:2].copy_(b[:1]) are grammarly correct as b's first shape is 1. If we wrongly write a's shape, grammar can be correct but semantic may not.