### **Project Checklist:**

1. [x] **Project Goals and Scope Defined**
2. [x] **Requirements Documented**
3. [ ] **Architecture Designed**
4. [ ] **Project Plan Created**
5. [x] **Version Control Set Up**
6. [ ] **Code Development Underway**
7. [ ] **Testing Completed**
8. [ ] **Documentation Prepared**
9. [ ] **Deployment and Monitoring Set Up**
10. [ ] **Maintenance Plan in Place**
#### plan for deleting entities from db:
- set isDeleted to true.
- create entry in "ThingsToDelete" table. This will have the following model:
	- ThingToDelete 
```json
{
		id: ObjectId,
		modelType: Type of model to be deleted,
		relatedId: id of entity to be deleted,
		TTL: time left to leave,
		dateCreated: DateTime,
		dateModified: DateTime,
		dateRead: DateTime
		}
```
- task should be scheduled that checks this table for items to delete and will delete them if their TTL is up, if not it updates dateRead and continues. If it gets to an entity whose dateRead matches "DateTime.now()", it skips it untill it's done reading the entire table.
- Then it closes




- [ ] junit
- [ ] bootstrapping springboot project
- [ ] refresh spring security
- [ ] hibernate and jpa
- [ ] finish project



.react-switch-checkbox {  
    height: 0;  
    width: 0;  
    visibility: hidden;  
}  
  
.react-switch-label {  
    display: flex;  
    align-items: center;  
    justify-content: space-between;  
    cursor: pointer;  
    width: 288px;  
    height: 60px;  
    background: grey;  
    border-radius: 30px;  
    position: relative;  
    transition: background-color .2s;  
}  
  
.react-switch-label .react-switch-button {  
    /*content: '';*/  
    position: absolute;  
    /*top: 2px;*/  
    left: 4px;  
    width: 140px;  
    height: 50px;  
    border-radius: 45px;  
    transition: 0.2s;  
    background: #fff;  
    box-shadow: 0 0 2px 0 rgba(10, 10, 10, 0.29);  
    /*z-index: 4;*/  
}  
  
.react-switch-button {  
    content: "Monthly";  
}  
  
.react-switch-checkbox:checked + .react-switch-label .react-switch-button {  
    left: calc(100% - 2px);  
    transform: translateX(-100%);  
}  
  
.react-switch-label:active .react-switch-button {  
    width: 60px;  
}  
  
.react-switch-labels {  
  /*display: relative;*/  
  z-index: 0;  
  height: 100%;  
  font: 14pt "Segoe UI", Verdana, sans-serif;  
}  
  
.react-switch-labels span {  
  position: absolute;  
  display: flex;  
  align-items: center;  
  justify-content: center;  
  width: 50%;  
  height: 100%;  
}  
.react-switch-labels span:first-child {  
  left: 0;  
}  
.react-switch-labels span:last-child {  
  right: 0;  
}