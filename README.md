# code-2
class node:

    def __init__(self,data):
        self.data=data
        self.next=None

class linked_list:

    def __init__(self):
        self.head=None


    def swap_pairs(self):

        p=self.head
        new_start=p.next

        t=self.head
        while(t):
            q=p.next
            temp=q.next
            q.next=p

            if(temp==None or temp.next==None ):
                p.next=None
                break

            
            p.next=temp.next
            p=temp
            

        t1=new_start
        while(t1):
            print(t1.data)
            t1=t1.next


    def insert(self,new_data):
        new_node=node(new_data)
        temp=self.head
        while(temp!=None and temp.next!=None):
            temp=temp.next

        if(temp!=None):
            temp.next=new_node

        else:
            temp=new_node
            self.head=new_node


    def print_list(self):
        temp=self.head
        while(temp):
            print(temp.data)
            temp=temp.next


if(__name__=='__main__'):

    llist=linked_list()
    llist.insert(1)
    llist.insert(2)
    llist.insert(3)
    llist.insert(4)
    llist.insert(5)
    llist.insert(6)
    print("The linked list is:")
    llist.print_list()
    print("The pairwise swapped nodes of the linked list is:")
    llist.swap_pairs()
    
