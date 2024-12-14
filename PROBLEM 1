class Book:
    def __init__(self, title, author, year, isbn):
        self.title = title
        self.author = author
        self.year = year
        self.isbn = isbn

    def __str__(self):
        return f"Title: {self.title}, Author: {self.author}, Year: {self.year}, ISBN: {self.isbn}"


class Library:
    def __init__(self):
        self.books = []

    def add_book(self, title, author, year, isbn):
        new_book = Book(title, author, year, isbn)
        self.books.append(new_book)
        print(f"Book '{title}' added to the library.")

    def display_books(self):
        if not self.books:
            print("No books in the library.")
        else:
            print("Books in the library:")
            for book in self.books:
                print(book)

    def search_books(self, title):
        found_books = [book for book in self.books if title.lower() in book.title.lower()]
        if found_books:
            print("Search results:")
            for book in found_books:
                print(book)
        else:
            print(f"No books found with title containing '{title}'.")


def main():
    library = Library()
    while True:
        print("\nLibrary Book Management System")
        print("1. Add a new book")
        print("2. Display all books")
        print("3. Search for a book by title")
        print("4. Exit")
        choice = input("Select an action (1-4): ")

        if choice == '1':
            title = input("Enter book title: ")
            author = input("Enter author name: ")
            year = int(input("Enter year of publication: "))
            isbn = input("Enter ISBN: ")
            library.add_book(title, author, year, isbn)

        elif choice == '2':
            library.display_books()

        elif choice == '3':
            title = input("Enter title to search for: ")
            library.search_books(title)

        elif choice == '4':
            print("Exiting the program.")
            break

        else:
            print("Invalid choice. Please select a valid action.")


if __name__ == "__main__":
    main()
