# githubTest
import argparse

def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

parser = argparse.ArgumentParser(description="Simple calculator CLI")
parser.add_argument("operation", choices=["add", "subtract"], help="Operation to perform")
parser.add_argument("a", type=int, help="First number")
parser.add_argument("b", type=int, help="Second number")

args = parser.parse_args()

if args.operation == "add":
    result = add(args.a, args.b)
elif args.operation == "subtract":
    result = subtract(args.a, args.b)

print("Result:", result)
