/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     struct ListNode *next;
 * };
 */
struct ListNode* swapPairs(struct ListNode* head) {
    struct ListNode*slow=head;
    struct ListNode*fast;
    if(head==NULL)
    {
        return head;
    }
    if(head->next!=NULL)
    {
    fast=head->next->next;
    }
    else
    {
        fast=NULL;
    }
    struct  ListNode*dummy=(struct ListNode*)malloc(sizeof(struct ListNode));
    dummy->val=0;
    struct ListNode*superslow=dummy;
    superslow->next=head;
    while(slow!=NULL)
    {
        struct ListNode*temp=slow->next;
        if(temp==NULL)
        {
            break;
        }
        slow->next=fast;
        superslow->next=temp;
        temp->next=slow;
        while(slow!=fast)
        {
            slow=slow->next;
        }
        while(superslow->next!=slow)
        {
            superslow=superslow->next;
        }
        if(fast==NULL) 
        {
            fast=NULL;
        }
        else if(fast->next==NULL)
        {
            fast=NULL;
        }
        else
        {
            fast=fast->next->next;
        }
    }
    return dummy->next;
}
