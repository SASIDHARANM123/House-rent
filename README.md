# House-rent
House rent code
location=["chennai","bangalore","kolkatta","Delhi"]
class admin:
    def addlocation(self,loc):
        location.append(loc)
    
    def removelocation(self,loc):
        location.remove(loc)
        
    def showlocation(self):
        print(location)

class user:
    def showlocation(self):
        print(location)


if __name__=="__main__":
    while(1):
        print("\nlogin as admin or user")
        print("Enter 1 for admin and 2 for user")
        inp=int(input())
        if inp==1:
            print("provide admin id:")
            admin_id="admin@123"
            print("provide password:")
            password="admin22"
            if admin_id=="admin@123" and password=="admin22":
                print("Loggedin as Admin successfully!!")
                ad1=admin()
                print("Admin operations:\n")
                print("Enter 1 for Add location")
                print("Enter 2 for Remove location")
                print("Enter 3 for show locations")
                oper=int(input())
                if oper==1:
                    loc=input("Enter location to add ")
                    ad1.addlocation(loc)
                    print("Location added successfully")
                elif oper==2:
                    loc=input("Enter location to remove ")
                    ad1.removelocation(loc)
                    print("Location removed successfully")
                elif oper==3:
                    ad1.showlocation()
                else:
                    print("Invalid input")
            else:
                print("Incorrect admin_id or password")
        elif inp==2:
            print("Loggedin as User successfully!!")
            user1=user()
            user1.showlocation()
        else:
            print("invalid input")
    
    
    
        

