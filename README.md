from telegram import Update
from telegram.ext import Application, CommandHandler

TOKEN = "8186874433:AAGlMY7eV6DNlZw794hz6mMkpLODi23KqmA"

async def start(update: Update, context):
    await update.message.reply_text("Hi, hello!")

def main():
    app = Application.builder().token(TOKEN).build()

    app.add_handler(CommandHandler("start", start))

    app.run_polling()

if __name__ == "__main__":
    main()
