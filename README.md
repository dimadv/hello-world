Questions:

1. There is string s = "string". Write the code that reverses string, i.e. returns "gnirts"

text = 'string'[::-1]
print(text)

2. What is the purpose of decorators?

Decorators are essentially "wrappers" that give us the ability to change the behavior of a function without changing its code.

3. Write decorator that measures function execution time and print it to output console.

def benchmark(func):
    import time
    
    def wrapper(*args, **kwargs):
        start = time.time()
        return_value = func(*args, **kwargs)
        end = time.time()
        print('[*] Время выполнения: {} секунд.'.format(end-start))
        return return_value
    return wrapper

@benchmark
def fetch_webpage(url):
    import requests
    webpage = requests.get(url)
    return webpage.text

webpage = fetch_webpage('https://google.com')
print(webpage)

# It is not my code, I copypaste it :(
# I understand that I should read more and more
# Good expirience :(

4.Create micro library that allows users to work with notes about books authors. Note should contain author_name, note, rating (rating - is 0 - 1 rating of the author) Micro lib should contain the next funcitonality:
Read notes from file
Add notes to file
Print notes to console
Get author with the highest rating
Get author with the lowest rating
Get average rating among all authors

NOT DONE:(
