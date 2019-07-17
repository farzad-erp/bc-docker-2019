code:


page 50109 ItemEntityApi2
{
    PageType = API;
    Caption = 'ItemEntityApi2';
    APIPublisher = 'bwg';
    APIGroup = 'group1';
    APIVersion = 'beta';
    EntityName = 'ItemEntityApi2';
    EntitySetName = 'ItemEntityApi2s';
    SourceTable = item;
    DelayedInsert = true;
    ODataKeyFields = Id;

    layout
    {
        area(Content)
        {
            repeater(GroupName)
            {
                field(MyField1; MyField1)
                {
                    Caption = 'MyField1';
                }

                // ###################################
                field(id; Id)
                {
                }
                
                
 normal api (doesn't include our api)
 http://bsuserpass06:7048/NAV/api/beta/$metadata
 
 see the api page in browser (UI Client)
 http://bsuserpass06/NAV/?bookmark=19%3bGwAAAAJ7BDEAMAAwADA%3d&page=50109&company=CRONUS%20UK%20Ltd.&dc=0
 
 
 see the path to our new api page (to consume)
 http://localhost:7048/NAV/api/bwg/group1/beta/companies(1b8d4e1a-577a-4831-b8aa-e6097e9f3887)/ItemEntityApi2s
 
 possible url to see only the extended api pages:
 http://localhost:7048/NAV/api/bwg/group1/beta/$metadata
 
 
 
 
 
 
               
