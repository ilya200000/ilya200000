-import telebot

bot = telebot.TeleBot("6548237199:AAHAdUk49czcfrtHBCTNbohrXeUDfofBlzs")
@bot.message_handler(commands=["donate"])
def donate(message):
    bot.send_message(message.chat.id, "подробное описание на https://project8086324.tilda.ws/sureland или тут /danatelist")
@bot.message_handler(commands=["donate1"])
def danate1(message):
    bot.send_message(message.chat.id,"вип - 5р.Возможности:/fly - включить/выключить полёт /ec - открыть личный виртуальный сундук /workbench - открыть верстак /getpos - узнать где свои координаты Префикс VIP в чате и табе, доступен титул Непобедимый для таба.")

@bot.message_handler(commands=["fly"])
def fly(message):
    bot.send_message(message.chat.id,"летать возможность VIP")

@bot.message_handler(commands=["ec"])
def ec(message):
    bot.send_message(message.chat.id,"открыть личный виртуальный сундук. Возможность VIP")

@bot.message_handler(commands=["workbench"])
def workbench(message):
    bot.send_message(message.chat.id,"открыть виртуальный верстак. Возможность VIP")

@bot.message_handler(commands=["donatelist"])
def danatelist(message):
    bot.send_message(message.chat.id, "/danote1 - VIP, Premium - /donate2")

@bot.message_handler(commands=["speed"])
def speed(message):
    bot.send_message(message.chat.id, "speed (0-10) - ускориться в ходьбе или полёте")

@bot.message_handler(commands=["anvil"])
def anvil(message):
    bot.send_message(message.chat.id, "открыть наковальню")

@bot.message_handler(commands=["cartographytable"])
def cartographytable(message):
    bot.send_message(message.chat.id, "открыть картографический стол")

@bot.message_handler(commands=["depth"])
def depth(message):
    bot.send_message(message.chat.id, "узнать уровень моря")


@bot.message_handler(commands=["donate2"])
def donate2(message):
    bot.send_message(message.chat.id, "/speed,/anvil,/cartographytable,/depth. Префикс Premium в чате и табе, доступен титул Редкий для таба.")


@bot.message_handler(commands=["start"])
def start(message):
    send_mess = f"<b>привет {message.from_user.first_name} {message.from_user.last_name} </b>!\nты в боте сервера sureland данат - /danate"
    bot.send_message(message.chat.id,send_mess,parse_mode="html")

bot.polling(none_stop=True)
