# tree_traversal_py

````py
class Node:
  def __init__(self, value):
    self.data = value
    self.left = None
    self.right = None

def pre_order(node):
  if node is not None:
    print(node.data)
    pre_order(node.left)
    pre_order(node.right)

def in_order(node):
  if node is not None:
    in_order(node.left)
    print(node.data)
    in_order(node.right)

def post_order(node):
  if node is not None:
    post_order(node.left)
    post_order(node.right)
    print(node.data)

def height(node):
  if node is None:
    return 0
  if node.left is None and node.right is None:
    return 0
  return 1 + max(height(node.left), height(node.right))
  
# create nodes
node1 = Node(1)
node2 = Node(10)
node3 = Node(11)
node4 = Node(20)
node5 = Node(25)
node6 = Node(30)
node7 = Node(40)
node8 = Node(100)

# establish the parent child relationships
node1.left, node1.right = node2, node3
node2.left, node2.right = node4, node5
node3.left, node3.right = node6, node7
node7.right = node8

# pre_order(node1)
# in_order(node1)
# post_order(node1)
# print(height(node1))

````
