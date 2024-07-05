class Contact:
    def _init_(self, name, phone, email):
        self.name = name
        self.phone = phone
        self.email = email

class ContactManager:
    def _init_(self):
        self.contacts = []

    def add_contact(self, contact):
        self.contacts.append(contact)
        print(f"Contact for {contact.name} added successfully.")

    def view_contacts(self):
        if not self.contacts:
            print("No contacts to display.")
        else:
            for contact in self.contacts:
                print(f"Name: {contact.name}, Phone: {contact.phone}, Email: {contact.email}")

    def search_contact(self, name):
        for contact in self.contacts:
            if contact.name.lower() == name.lower():
                print(f"Found contact: Name: {contact.name}, Phone: {contact.phone}, Email: {contact.email}")
                return
        print(f"No contact found with name {name}")

    def delete_contact(self, name):
        for contact in self.contacts:
            if contact.name.lower() == name.lower():
                self.contacts.remove(contact)
                print(f"Contact for {contact.name} deleted successfully.")
                return
        print(f"No contact found with name {name}")

def main():
    manager = ContactManager()

    while True:
        print("\nContact Management System")
        print("1. Add Contact")
        print("2. View Contacts")
        print("3. Search Contact")
        print("4. Delete Contact")
        print("5. Exit")

        choice = input("Enter your choice: ")

        if choice == '1':
            name = input("Enter name: ")
            phone = input("Enter phone: ")
            email = input("Enter email: ")
            contact = Contact(name, phone, email)
            manager.add_contact(contact)
        elif choice == '2':
            manager.view_contacts()
        elif choice == '3':
            name = input("Enter name to search: ")
            manager.search_contact(name)
        elif choice == '4':
            name = input("Enter name to delete: ")
            manager.delete_contact(name)
        elif choice == '5':
            print("Exiting...")
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
