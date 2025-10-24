# ==================================
# Project: Robust Coding Foundation for the 
# Description:
# A robust foundation for coding experiments and future projects.
# Focus: Reliable, Scalable, Well-Structured Code 
# ================================

# ---------- main.py ----------
"""
Main entry point for the project.
A robust foundation for coding experiments and future projects.
"""

from core import utils, experiments


def run():
    print("🚀 Starting Project Foundation")
    print("📚 Reliable, Scalable, Well-Structured Code\n")

    # Example usage
    print("Random Number:", utils.generate_random_number())
    print("Fibonacci(10):", experiments.fibonacci(10))


if __name__ == "__main__":
    run()


# ---------- core/utils.py ----------
"""
Utility functions for the project.
These can be reused across multiple experiments and modules.
"""

import random

def generate_random_number(min_val=1, max_val=100):
    """Return a random integer between min_val and max_val."""
    return random.randint(min_val, max_val)

def is_even(n: int) -> bool:
    """Check if a number is even."""
    return n % 2 == 0


# ---------- core/experiments.py ----------
"""
Module for coding experiments and prototypes.
"""

def fibonacci(n: int) -> list:
    """Return a list of the first n Fibonacci numbers."""
    if n <= 0:
        return []
    seq = [0, 1]
    while len(seq) < n:
        seq.append(seq[-1] + seq[-2])
    return seq[:n]


# ---------- tests/test_utils.py ----------
"""
Basic test cases for utils.py
Run with: pytest
"""

from core import utils

def test_generate_random_number():
    num = utils.generate_random_number(1, 10)
    assert 1 <= num <= 10

def test_is_even():
    assert utils.is_even(2) is True
    assert utils.is_even(3) is False
