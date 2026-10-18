import asyncio
from telegram import Update
from telegram.ext import Application, CommandHandler, MessageHandler, filters, ContextTypes

async def start(update: Update, context: ContextTypes.DEFAULT_TYPE):
    await update.message.reply_text('你好！我已經成功連上程式碼了！')

async def echo(update: Update, context: ContextTypes.DEFAULT_TYPE):
    user_text = update.message.text
    await update.message.reply_text(f'你傳了：{user_text}')

def main():
    TOKEN = '8804835471:AAEuY7s8qKk2gF55EQQlPjCzTPUPTBYLhCU'
    
    app = Application.builder().token(TOKEN).build()
    app.add_handler(CommandHandler("start", start))
    app.add_handler(MessageHandler(filters.TEXT & ~filters.COMMAND, echo))
    
    print("機器人已啟動，請去 Telegram 測試...")
    app.run_polling()

if __name__ == '__main__':
    main()
