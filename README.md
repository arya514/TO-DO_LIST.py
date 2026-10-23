tasks=[]
while True :

    print("\n TO DO LIST ")
    print("1.add task")
    print("2.view your tasks")
    print("3.mark your task done")
    print("4.exit")

    choice = int(input("enter your choice (1-4) : "))

    if choice == 1 :
        task = input(" enter your task : ")
        tasks.append(task)
        print("task added successfully")

    elif choice == 2 :
        if len(tasks) == 0 :
            print(" no tasks are available ")
        else :
            for i in range (len(tasks)) :
                print(f"{i+1} , {tasks[i]}")  

    elif choice == 3 :
        if len(tasks) == 0:
            print (" no tasks are available to mark as done ")
        else :
            task_no = int(input("enter the task number mark as done :"))
            if 1 <= task_no <= len(tasks) :
                done_task = tasks.pop(task_no - 1)
                print(f"task {done_task} marked as done !")

    elif choice == 4 :
        print("exiting to do list , goodbye ")
        break
    else :
        print(" invalid choice , please try again ")
