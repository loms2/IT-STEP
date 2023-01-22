class Human:
    def __init__(self, name: str, age: int, height: int):
        self.name = name
        self.age = age
        self.height = height
    def life(self):
        print("I live")


class Father(Human):
    def __init__(self, name, age, height, muscles = 10):
        super().__init__(name, age, height)
        self.muscles = muscles
    def push_up(self):
        self.muscles += 1
        print("I am strong")


class Mather(Human):
    def __init__(self, name, age, height, cooking = "Master"):
        super().__init__(name, age, height)
        self.cooking = cooking
    def cook(self):
        print("I love cooking")


class Brother(Father):
    def __init__(self, name, age, height, muscles, favorit_game= "Minecraft"):
        super().__init__(name, age, height, muscles)
        self.favorit_game = favorit_game
    def play_game(self):
        print(f"My favorit game is {self.favorit_game}")


class Sister(Mather):
    def __init__(self, name, age, height, cooking = "terribly", Followers = 0):
        super().__init__(name, age, height, cooking)
        self.Followers =Followers
    def Instagram(self):
        print(f"I have {self.Followers} followers")


H = Human("Man", 100, 200)
F = Father("Taras", 39, 183, 7)
M = Mather("Oksana", 39, 167, "Super")
B = Brother("Anton", 15, 175, 12, "Dota 2")
S = Sister("Anima", 12, 154, "Master", 1277)
