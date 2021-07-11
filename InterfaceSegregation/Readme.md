# Interface Segregation Principle

<h2 align="center">Simple Definition : </h2>

   Clients shouldn't be forced to depend on methods they don't use.

<h2 align="center">Publish-Subscribe</h2>

- **Channel**: represent the idea of an invokable collection of subscribers.
- **Subscriber:** represent the receiver of the message
- **Publisher:** represent the sender of the message

> By segregating the subscriber and publisher will make your code more easy and huge architectural benefit. If you know the problem in PUB-SUB architectural pattern.  

<h2 align="center">Key Points</h2>

1. Explicit and clear dependencies.
2. More readable code without puzzling empty methods.
3. Easy to find all clients which are intreseted in a specific message.
4. Safe and easy addition of new message types in the future.

<h2 align="center">Summary.</h2>

- [x] ISP is a principle of least knowledge and information hiding.
- [x] Publish - Subscriber pattern and Big callback interfaces.

<h2 align="center">Benefits.</h2>

- [x] Allows you to communicate what clients **DO** with their services.
- [x] Allows you to communicate what clients **DON'T DO** with their services.
- [x] Restrict what clients **CAN DO** with their services.
- [x] Segregated interfaces allow to segregate functionality if/when needed.
