# Messenger Logger
try:
    print("(debug, info, warning, error, critical)")
    switch = True
    i = 0
    amountOfAttempts = 4
    print("Reminder1: Ctrl+C to terminate")
    print("Reminder2: See results after completing program")
    import logging
    logging.basicConfig(level=logging.DEBUG, filename="none.log",filemode="a",
                            format="%(asctime)s - %(filename)s - %(levelname)s - %(name)s - %(message)s")
    logger = logging.getLogger(__name__)
    fHandler = logging.FileHandler("messengerlog.log")
    sHandler = logging.StreamHandler()
    fHandler.setLevel(logging.DEBUG)
    sHandler.setLevel(logging.DEBUG)
    formatter = logging.Formatter("%(asctime)s|%(levelname)s|%(message)s")
    fHandler.setFormatter(formatter)
    sHandler.setFormatter(formatter)
    logger.addHandler(fHandler)
    logger.addHandler(sHandler)
    print("Message Program by John Renconada!")
    # print("(debug, info, warning, error, critical)")
    levels = ["debug", "info", "warning", "error", "critical"]
    while (i<=amountOfAttempts):
        usrUsername = str(input("Enter Username: "))
        usrLevelPrompt = str(input("Enter Message Level: "))
        lowerUsrLevelPrompt = usrLevelPrompt.lower()
        if lowerUsrLevelPrompt == levels[0]:
            print("Message Level > Debug")
            usrInput = input(f"{usrUsername} Message: ")
            logger.debug(f"{usrUsername}:\"{str(usrInput)}\"")
        elif lowerUsrLevelPrompt == levels[1]:
            print("Message Level > Info")
            usrInput = input(f"{usrUsername} Message: ")
            logger.info(f"{usrUsername}:\"{str(usrInput)}\"")
        elif lowerUsrLevelPrompt == levels[2]:
            print("Message Level > Warning")
            usrInput = input(f"{usrUsername} Message: ")
            logger.warning(f"{usrUsername}:\"{str(usrInput)}\"")
        elif lowerUsrLevelPrompt == levels[3]:
            print("Message Level > Error")
            usrInput = input(f"{usrUsername} Message: ")
            logger.error(f"{usrUsername}:\"{str(usrInput)}\"")
        elif lowerUsrLevelPrompt == levels[4]:
            print("Message Level > Critical")
            usrInput = input(f"{usrUsername} Message: ")
            logger.critical(f"{str(usrUsername)}:\"{str(usrInput)}\"")
except KeyboardInterrupt as e:
    print("Terminated")
    logger.exception("Chat Ended", exc_info=False)
except ValueError as e:
    print("Invalid Input")
    logger.exception("Chat Ended", exc_info=False)
except OSError as e:
    print(e)
    logger.exception("Chat Ended", exc_info=False)
