# new_model_jaa


changed in crud.py and main

current_date =  current_date = date.today()

@app.post("/update-total-time/")
async def update_total_time(user_id: int, service_id: int, db: Session = Depends(get_db)):

    crud.fetch_total_time(db, user_id, service_id)
    return {
        "message": "Total time updated successfully",
        "user_id": user_id,
        "service_id": service_id
    }
